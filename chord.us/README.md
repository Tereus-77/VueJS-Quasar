# Chord Video (chord.us)

Chord Video

## Install the dependencies

```bash
npm install
```

### Start the app in development mode (hot-code reloading, error reporting, etc.)

```bash
quasar dev
```

### Lint the files

```bash
npm run lint
```

### Build the app for production

```bash
sudo npm run build
```

### Customize the configuration

See [Configuring quasar.conf.js](https://quasar.dev/quasar-cli/quasar-conf-js).

## Component Folder Structure and Naming Conventions

The project adheres to the VueJS styleguide for naming components. There are three types of components:

1. Base Components
2. Root Components
3. Child Components

Each follows rules surrounding folder structure and naming conventions to make organizing the code easier, and to reduce cognitive overhead.
All Components have their root in the `./src/components/` folder.

### Base Components

Base Components serve as a "template" or "Super" component which other components can extend to include shared functionality in addition to their specific purpose.

#### Naming Convention

Base Components should always be **prefixed** with `Base` to indicate their purpose. Other components which would extend a Base Component will typically be Root Components in their own
right, but should drop the `Base` **prefix**, and use the rest of the Base Component's name as a **suffix** instead.

##### Examples

A base card component:

- `BaseCard`

Any components extending it should be named for their function with `Card` as the **suffix**:

- `ProfileCard`
- `ItemCard`

#### Folder Structure

All Base Components should reside in the `/src/components/Base/` folder:

##### Example

```js
.
└─ src/
   └─ components/
      └─ Base/
         └─ BaseCard.vue
```

### Root Components

Root Components are independent components that serve a specific purpose, also known as containers or "Smart" components.

#### Naming Convention

Root Components should always be multi-word (never a single name, for reasons outlined in the VueJS styleguide), with each word being delimited by a capital letter and should give an indication of their purpose.
Root Components that are related in function can be grouped together and identified by a common **suffix**, and are commonly referred to as a "collection".

##### Examples

A singular Root Component for a meeting room:

- `MeetingRoom`

A collection of related Root Componments representing common controls:

- `AudioControl`
- `VideoControl`
- `FullScreenControl`

#### Folder Structure

Singular Root Components should have their own folder (even if it only contains one component) since Child Components should live within the same folder as their parent.
Collections should share a folder derived from the pluralized version of their common **suffix**.

##### Examples

The `MeetingRoom` example from above would be:

```js
.
└─ src/
   └─ components/
      └─ MeetingRoom/
         └─ MeetingRoom.vue
```

The collection example from above would look like:

```js
.
└─ src/
   └─ components/
      └─ Controls/
         ├─ AudioControl.vue
         ├─ VideoControl.vue
         └─ FullScreenControl.vue
```

### Child Components

Child Components are components which function specifically as children of (and are therefore dependent on) a Root Component, or even another Child Component.

#### Naming Convention

Child Components should adopt their parent's name as a **prefix** to indicate that they are children of that component.

##### Example

Let's use the `MeetingRoom` Root Component from above. If it has two child components, say a toolbar and a profile card (which extends the `BaseCard` in this example):

- `MeetingRoomToolbar`
- `MeetingRoomProfileCard`

#### Folder Structure

Child Components should always live in the same folder as their parent. The above example would be:

```js
.
└─ src/
   └─ components/
      └─ MeetingRoom/
         ├─ MeetingRoom.vue
         ├─ MeetingRoomToolbar.vue
         └─ MeetingRoomProfileCard.vue
```

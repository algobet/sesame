# sesame
Official lightweight javascript framework of Digital Asset Simulator (DAS) protocol atop the IPFS.

## Install, Build and Test
```
$ npm install
$ npm run build
$ npm run start
```

## Simulation Specs
\#Hash \#Repository \#Badge \#Issue

### BAO

| Property | Expected Type | Description |
| -------- | ------------- | ----------- |
| **id** | ID | Unique ID the bao.
| **type** | BaoType |
| **assetType** | Containing asset type |
| **recipient** | Recipient | The recipient object of this bao.
| **asset** | @id: Any | Unique IRI for the associated object
| **verification** | Text | Signed token or hash (identity+passcode)
| **issuedOn** | DateTime | Timestamp of when the bao was issued

### Recipient

| Property | Expected Type | Description |
| -------- | ------------- | ----------- |
| **type** | IdentityType |
| **identity** | Text | Either the hash of the identity or the plaintext value.
| **hashed** | Boolean | Whether or not the identity value is hashed.
| **salt** | Text |

### Sender

| Property | Expected Type | Description |
| -------- | ------------- | ----------- |
| **type** | ProfileType |
| **name** | Text | Name of this profile |
| **account** | Text | A hash code representation of this profile

### Badge

| Property | Expected Type | Description |
| -------- | ------------- | ----------- |
| **type** | Text | Badge
| **name** | Text | The name of the achievement.
| **description** | Text | A short description of the achievement.
| **image** | @id: Image | Unique IRI of an image representing the achievement.
| **issuer** | @id: Sender | Unique IRI or document describing the individual, entity, or organization that issued the badge.


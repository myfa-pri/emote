# Emote API (Free Fire)

API to trigger/run an emote on a Free Fire account using **UID** and **emote ID**.

## Base URL

`https://myfa-ffinfo.vercel.app`

---

## Endpoint

### Run Emote

**GET**
`/emote-run?uid={USER_UID}&emoteId={EMOTE_ID}`

### Example Request

```bash
curl "https://myfa-ffinfo.vercel.app/emote-run?uid=12239804529&emoteId=17"
```

Or in browser:

`https://myfa-ffinfo.vercel.app/emote-run?uid=12239804529&emoteId=17`

---

## Parameters

- `uid` (required)  
  Free Fire player UID  
  Example: `12239804529`

- `emoteId` (required)  
  Emote ID to run  
  Example: `17`

---

## Response Format

### Success
```json
{
  "success": true,
  "uid": "12239804529",
  "emoteId": "17",
  "message": "Emote executed successfully"
}
```

### Error
```json
{
  "success": false,
  "message": "Invalid UID or emoteId"
}
```

---

## Existing Player Info Endpoint

You can also fetch player information:

**GET**
`/player-info?uid={USER_UID}`

Example:
`https://myfa-ffinfo.vercel.app/player-info?uid=12239804529`

---

## Notes

- Make sure the UID is valid.
- Make sure `emoteId` exists and is allowed.
- API should return proper errors for invalid inputs.
- Use responsibly and only on accounts you own/manage.

---

## Quick Test URLs

- Player info:  
  `https://myfa-ffinfo.vercel.app/player-info?uid=12239804529`

- Run emote:  
  `https://myfa-ffinfo.vercel.app/emote-run?uid=12239804529&emoteId=17`
# Contributor Reward Layer - Architecture Docs

## Workflow Flowchart
[User/Contributor] 
       │
       ▼ (Submits Github PR or Discord Task via Rooms UI)
[Rooms.run Frontend]
       │
       ▼ (API Request with Signed Solana Message)
[Rooms-Contributor-Core Backend] ───► (Verifies Signature via tweetnacl)
       │
       ├─► (Checks GitHub API / Task Verification)
       │
       ▼ (If valid, triggers Anchor/Solana Program)
[Solana Blockchain] ───► (Distributes Token Rewards via SPL Token Mint)

# Mind X Parts Room

A private, browser-to-browser visual workspace for exploring inner parts, roles, protective patterns, needs, and relationships.

## Features

- Fully static and ready for GitHub Pages
- Two-person synchronization through WebRTC data channels
- Manual offer/answer exchange without an application database
- Private solo mode
- Client-led editing permissions
- Shared therapist pointer
- Draggable, resizable, renameable, and recolorable parts
- Multiple part shapes and customizable center
- Relationship lines for connection, distance, alliance, tension, and influence
- Reflection invitations
- Undo and redo
- Local PNG and JSON export
- Local JSON import
- Dark mode
- Responsive desktop, tablet, and mobile interface
- English edition at `/`
- Simplified and Traditional Chinese in one page at `/zh/`

## Deploy to GitHub Pages

1. Create a GitHub repository.
2. Upload everything inside this package to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.

The English edition will be at the repository root. The Chinese edition will be at `/zh/`.

## Connecting two browsers

1. One participant chooses **Create connection**.
2. Wait until the status confirms that the complete offer is ready.
3. Send the complete offer through an agreed private channel.
4. The second participant chooses **Join connection**, pastes the offer, and selects **Create answer**.
5. Wait until the complete answer is ready and send it back.
6. The first participant pastes the answer and selects **Finish connection**.

The codes contain WebRTC connection information. They expire when the page is closed and should still be exchanged privately.

## Network limitation

The application uses Cloudflare's public STUN endpoint for network discovery. It does not include a TURN relay or signaling server. Direct connections will work on many networks but may fail on restrictive corporate, institutional, cellular, or symmetric-NAT networks. GitHub Pages cannot provide TURN.

A later deployment can add a self-hosted signaling and TURN service without replacing the Parts Room interface.

## Privacy and clinical use

- The website has no account system, analytics, recording, transcript, or server-side session database.
- Workspace content is not uploaded by the application.
- PNG and JSON files are created only after the user deliberately requests an export.
- Network and STUN providers may still receive connection metadata.
- WebRTC encryption does not independently establish legal or regulatory compliance.
- Users should minimize identifying information and follow applicable laws, professional ethics, organizational policies, and informed-consent requirements.

This is a reflective collaboration tool—not an emergency service, diagnostic instrument, clinical record, or autonomous treatment.

## Testing

WebRTC and clipboard behavior should be tested through HTTPS or localhost. Test with two separate devices or browser profiles, including a cellular or external network.

## License

MIT. See `LICENSE`.

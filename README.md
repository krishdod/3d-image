AR Photo Video

Scan a printed photo with your phone and play a video (with music) on top of it using WebAR (A-Frame + AR.js NFT).

Folder Structure

ar-photo-video/
├── index.html            # main AR page
├── video.mp4             # your video with music (add your own)
├── marker/               # NFT marker files (replace with your own)
│   ├── photo.fset
│   ├── photo.fset3
│   └── photo.iset

1) Add Your Video

- Put your video file at the project root named "video.mp4".
- Keep it small for mobile (ideally under ~20–40 MB).

2) Generate NFT Marker Files

You need three files for your photo target: photo.fset, photo.fset3, photo.iset.

Option A: Online NFT Marker Creator
- Use the AR.js NFT marker creator (web UI). Upload your photo and download the three files.
- Place them in marker/ and keep the base name "photo".

Option B: Local/GitHub Generator (if the online tool doesn’t load)
- Install Node.js (LTS), clone the AR.js NFT builder, and run the generator against your image to produce *.fset, *.fset3, *.iset.
- Rename to photo.fset, photo.fset3, photo.iset and place into marker/.

Tips for tracking
- Use a photo with high-contrast, non-repeating details.
- Avoid glossy reflections and large uniform areas.
- Print at least postcard size; keep it flat and well lit.

3) Run Locally (optional)

- Serving over HTTPS is best for camera permissions. Quick dev options:
  - VS Code Live Server
  - npx http-server -p 8080 (open http://<your-ip>:8080 on your phone on same Wi‑Fi)

4) Host for Free

- GitHub Pages, Netlify, or Vercel all work. Upload all files including marker/ and video.mp4.

5) Test on Your Phone

1. Print the same photo used to generate the marker.
2. Open your hosted page URL on the phone.
3. Allow camera access.
4. Tap the green "Tap to start AR" button to enable audio.
5. Point the camera at the printed photo. The video should play on top with sound.

Troubleshooting

- No sound: Make sure you tapped the start button once.
- Marker not recognized: Use a more feature-rich image, improve lighting, keep print flat.
- Performance: Reduce video resolution/bitrate; ensure the image has sufficient features.

Customize

- Adjust the a-video width/height in index.html to match your photo’s aspect.
- You can start muted and unmute after the user gesture if needed.



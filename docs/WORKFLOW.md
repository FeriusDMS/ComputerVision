## Workflow

### Image Processing Workflow
1. **Input**: Load image(s) containing faces
2. **Detection**: Detect all faces in the image
3. **Extraction**: Extract facial regions and landmarks
4. **Selection**: Choose replacement faces (random or specified)
5. **Alignment**: Align replacement faces with detected faces
6. **Swapping**: Perform face swap with color/lighting adjustment
7. **Blending**: Blend swapped faces seamlessly into the original image
8. **Output**: Save anonymized image(s)

### Video Processing Workflow (NEW! 🎬)
1. **Input**: Load MP4 video file
2. **Source Loading**: Load source face image for swapping
3. **Frame Analysis**: Process each frame sequentially
4. **Face Detection**: Detect faces in current frame (Haar + equalization)
5. **Landmark Detection**: Extract 68 facial landmarks (with cache)
6. **Logic Selection**:
   - 1 face → Swap with source
   - 2 faces → Mutual swap
   - 3+ faces → All swap with source
7. **Validation**: Multi-level validation of landmarks and triangles
8. **Swapping**: Triangle-based warping with seamless cloning
9. **Blending**: Natural blending with improved masking
10. **Output**: Write processed frame to output video
11. **Statistics**: Track success/failure rates and face counts
12. **Preview**: Display sample frames during processing

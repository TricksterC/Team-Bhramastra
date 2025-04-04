# Team-Bhramastra 🚀
Coding project for Honeywell's Hackathon that converts point clouds to 3d meshes.


**Point Cloud to 3D Mesh Converter**  
A desktop application for 3D point cloud processing with surface reconstruction and multi-format export capabilities.  

---

**Key Features**  
- **User friendly GUI Interface**: File input dialog with format filtering  
- **Input Compatibility**: `.pcd`, `.xyz`, `.ply`, `.obj` files (also  `.e57` files with additional manipulation)
- **Processing Pipeline**:  
  1. Normal estimation with KD-tree optimization  
  2. Consistent normal orientation  
  3. Dual reconstruction engines:  
     - Poisson (adaptive depth)  
     - Ball Pivoting (radius auto-calibration)  
- **3D Visualization**: Interactive preview with rotation/zoom  
- **Multi-Format Export**: `.stl`, `.ply`, `.obj`
- **Higher Accessibility:** Improves range of devices by allowing preview to be saved in `.gif` format

**Workflow Process**  
1. Users select a point cloud file via the GUI  
2. System processes data with Open3D backend  
3. Live preview shows original cloud + reconstructed mesh  
4. The export panel offers format selection and save location 

**Technical Foundation**  
- Core Engine: Open3D for geometric processing  
- Visualization: Integrated 3D viewport with camera controls  
- Export System: Format conversion with vertex normal preservation  
- Cross-Platform: Works on Windows/macOS (path handling optimized)  

**Dependencies**  
- Open3D >= 0.17.0  
- NumPy  
- PyQt5 (GUI framework)  
- ImageIO (for future animation features)  

**I/O Specifications**  
|||
|-|-|
|**Input**|**Output**|  
|Point Clouds (.pcd/.xyz/.ply/.obj)|Meshes (.stl/.ply/.obj) and Image (.gif)|  

**Achievements with current solution:**  
1. Successfully executed conversion of point cloud file with approximately 6 lakh points (with considerable attention to detail)
2. Successfully made colored output files
3. Successfully added-on texture (from existing data in the source file)

**Future prospects:**  
- Implementation of an AI model to allow object detection within a given Point cloud file after processing
- Addition of voxel downsampling and/or advanced noise reduction 
- Implementation of Deep learning concepts to make a "one-size-fits-all" solution for increased robustness



**Research and References:**
1. F. Z. Iguenfer, A. Hsain, H. Amissa, and Y. Chtouki, "Point cloud to mesh reconstruction: A focus on key learning-based paradigms," School of Science and Engineering, Al Akhawayn University, Ifrane, Morocco.
2.  Florent Poux, "5-Step Guide to Generate 3D Meshes from Point Clouds with Python," 2023. [Online].
3.  C. R. Qi, H. Su, K. Mo, and L. J. Guibas, "PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation," in 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), Honolulu, HI, USA, 2017, pp. 652-660, doi: 10.1109/CVPR.2017.16.
4.  C. R. Qi, L. Yi, H. Su, and L. J. Guibas, "PointNet++: Deep Hierarchical Feature Learning on Point Sets in a Metric Space," in Advances in Neural Information Processing Systems (NeurIPS), 2017, pp. 5099–5108.
5.  S. V. Sheshappanavar and C. Kambhamettu, "A Novel Local Geometry Capture in Pointnet++ for 3D Classification," 2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), Seattle, WA, USA, 2020, pp. 1059-1068, doi: 10.1109/CVPRW50498.2020.00139.



Key Components in IEEE Format:

**Test files:**
Since GitHub's free version doesn't allow files above 25MB, use this link to download the sample files that were used to implement this program: https://drive.google.com/drive/folders/18X2kSOcFMKkZLnzxCQbbNFFOxBOyrdFk?usp=sharing

**Cross-Platform Note**: While core functionality works universally, file dialogs/paths auto-adapt to OS conventions.

## Presented by

- Priyanshu Tiwari - Project Lead & Algorithm Developer - 3rd Year AI/ML student at Sir M Visvesvaraya Institute of Technology
- N Ram Srujan Raj - 3D Parsing Specialist & Core Engineer - 1st Year CSE student at Sir M Visvesvaraya Institute of Technology
- Rishabh Raj - UI/UX Designer - 2nd Year ISE student at Sir M Visvesvaraya Institute of Technology
- Aditya Kumar - System Integrator - 2nd year ISE student at RV Institute of Technology and Management 

## Mentor
- Dr S Ambareesh (Professor in AI/ML at Sir M Visvesvaraya Institute of Technology)

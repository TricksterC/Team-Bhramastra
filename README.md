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


# **Demo** 

# Raw Point Cloud 
<img width="710" alt="Screenshot 2025-04-04 at 7 13 29 AM" src="https://github.com/user-attachments/assets/ec15775a-d14b-4510-a129-4849432fca6a" />

![rotating_3d_view](https://github.com/user-attachments/assets/0c65f7aa-8669-4e17-b437-c205b32bac88)

# Point cloud with Normals
<img width="710" alt="Screenshot 2025-04-04 at 7 26 11 AM" src="https://github.com/user-attachments/assets/205f71a8-1431-4a73-924c-82fca015fc61" />

![point cloud normal_view](https://github.com/user-attachments/assets/351f19e7-db45-45cb-a4c1-7c1a23cc620c)


# point cloud with poisson Mesh
<img width="710" alt="Screenshot 2025-04-04 at 7 14 12 AM" src="https://github.com/user-attachments/assets/c22c0655-5f29-4407-9f6a-facf7599bb99" />

![rotating_3d_view](https://github.com/user-attachments/assets/2001add9-ddc3-4822-be69-f0dad543c821)

# Ball pivoting Mesh 
<img width="710" alt="Screenshot 2025-04-04 at 7 25 36 AM" src="https://github.com/user-attachments/assets/42934936-fafb-4f57-93ee-e8804f6f6ba0" />

![Ball Pivoting](https://github.com/user-attachments/assets/91a06958-1474-4c9e-9d72-2a6440bf6d8c)

# compare Meshes
<img width="1710" alt="Screenshot 2025-04-04 at 7 15 08 AM" src="https://github.com/user-attachments/assets/ceb2d209-6390-4a4b-ba20-2a5ba8ed0d43" />
=======


**Research and References:**
1. F. Z. Iguenfer, A. Hsain, H. Amissa, and Y. Chtouki, "Point cloud to mesh reconstruction: A focus on key learning-based paradigms," School of Science and Engineering, Al Akhawayn University, Ifrane, Morocco.
2.  Florent Poux, "5-Step Guide to Generate 3D Meshes from Point Clouds with Python," 2023. [Online].
3.  C. R. Qi, H. Su, K. Mo, and L. J. Guibas, "PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation," in 2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR), Honolulu, HI, USA, 2017, pp. 652-660, doi: 10.1109/CVPR.2017.16.
4.  C. R. Qi, L. Yi, H. Su, and L. J. Guibas, "PointNet++: Deep Hierarchical Feature Learning on Point Sets in a Metric Space," in Advances in Neural Information Processing Systems (NeurIPS), 2017, pp. 5099–5108.
5.  S. V. Sheshappanavar and C. Kambhamettu, "A Novel Local Geometry Capture in Pointnet++ for 3D Classification," 2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), Seattle, WA, USA, 2020, pp. 1059-1068, doi: 10.1109/CVPRW50498.2020.00139.


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

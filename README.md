# Tutorial Flexible Docking menggunakan AutoDock-GPU pada Windows
1. pythonsh prepare_flexreceptor.py -r 1fpu_receptor.pdbqt -s THR315
2. pythonsh prepare_gpf.py -l lig.pdbqt -r rec_rigid.pdbqt -y
3. autogrid4 -p rec_rigid.gpf -l rec_rigid.glg
4. adgpu --ffile rec_rigid.maps.fld --flexres rec_flex.pdbqt --lfile lig.pdbqt --nrun 100 --gbest best.pdbqt
5. obabel best.pdbqt -O results.pdb

# Tutorial Flexible Docking menggunakan AutoDock-GPU pada Linux
1. pythonsh prepare_flexreceptor.py -r 1fpu_receptor.pdbqt -s THR315
2. pythonsh prepare_gpf.py -l lig.pdbqt -r rec_rigid.pdbqt -y
3. autogrid4 -p rec_rigid.gpf -l rec_rigid.glg
4. adgpu --ffile rec_rigid.maps.fld --flexres rec_flex.pdbqt --lfile lig.pdbqt --nrun 100 --gbest best.pdbqt
5. obabel best.pdbqt -O results.pdb

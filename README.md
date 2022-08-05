# Tutorial Flexible Docking

pythonsh prepare_flexreceptor.py -r 1fpu_receptor.pdbqt -s THR315
pythonsh prepare_gpf.py -l lig.pdbqt -r rec_rigid.pdbqt -y
autogrid4 -p rec_rigid.gpf -l rec_rigid.glg
adgpu --ffile rec_rigid.maps.fld --flexres rec_flex.pdbqt --lfile lig.pdbqt --nrun 100 --gbest
obabel best.pdbqt -O results.pdb

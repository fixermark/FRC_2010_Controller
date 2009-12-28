Important Changes for teams using LabVIEW

VIs related to updating the dashboard data changed and are incompatible with previous versions.  If you go through the wizard to create a new project everything will work, however if you want to update an existing project you will need to make a few edits.

Set User Data.vi in DriverStation.lvlib has been removed, if your code used this VI, replace it with Set High Priority Dashboard Data.vi

Dashboard Enable.ctl has been moved out of vi.lib\Robotics Library\WPI\Driver Station\ into the user project code.  This will cause a linking problem for existing projects which use Build Dashboard Data.vi.  Two solutions exist, the first is to right click the Dashboard Enabled control on the front panel of Build Dashboard Data.vi and select "Disconnect from Type Def."  The second option is to copy the file from C:\Program Files\National Instruments\LabVIEW 8.6\resource\plugins\NewDialogFiles\ProjectWizards\FRC\FRC Templates\Robot\Real VIs\DashboardEnable.ctl into your project folder, then right click the control in Build DashBoard Data.vi and select Replace -> Select A Control... and choose the DashboardEnable.ctl you just copied into your project's folder.
 
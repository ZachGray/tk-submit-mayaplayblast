tk-submit_mayaplayblast
=====================
###Description:

Application to playblast assets or shots.

####Dependencies:<br>
**https://github.com/shotgunsoftware/python-api**
<br>
####General application notes:<br>
It is important to note using dev path will cause some **cross platform** issues because you'll end up with a hard coded path.<br>
To avoid this you can copy the application into the studio/install/apps/app_store/ directory and use:<br>
`location: {name: tk-jbd-submit-mayaplayblast, type: app_store, version: v0.0.1}`<br>
**HOW EVER!**<br>
*__This will cause tank updates to fail because the applications don't exist in the official app store__*<br>
So before doing a tank update you'll need to remove or change these paths back to dev!<br>
<br>
<hr>
#APPLICATION INSTALL NOTES:
* **You must have the python-api installed for shotgun!**
* Adding to the asset_step and shot_step:
```
      tk-submit-maya-shotPlayblast:

            location:                   {name: tk-jbd-submit-mayaplayblast, type: dev, path: 'path/to/install/directory'}
            display_name:               .Publish TurnTable For Review...
            cameraSuffix:               _shotCam
            isAsset:                    true
            movie_width:                1280
            movie_height:               720
            movie_path_template:        maya_asset_playblast
            movie_workpath_template:    maya_assetwork_playblast
            new_version_status:         rev
            sg_in_frame_field:          sg_cut_in
            sg_out_frame_field:         sg_cut_out
            store_on_disk:              true
            template_work:              maya_asset_work
            upload_to_shotgun:          true
            version_number_padding:     3
```
<br>
<center>
<img src = "http://www.anim83d.com/images/github/mpb_01.PNG"><br>
<img src = "http://www.anim83d.com/images/github/mpb_02.PNG"><br>
More to come...
</center>
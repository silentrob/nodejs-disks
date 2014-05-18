nodejs-disks
============

Gets current disk information from Server hosting nodejs application.

This was derived from the original creator project, node-diskfree by Ismael Gorissen (pinchprojectbackend) it is available at https://bitbucket.org/pinchprojectbackend/node-diskfree/ license for this project is shown in OriginalLicense.md

I have added the drive mountpoint name as well as calculating the percentage of used space and percentage of free space.

Usage

var df = require('nodejs-disks');

df.drives(
            function (err, drives) {
                if (err) {
                    return console.log(err);
                }

                /* retrieve space information for each drives */
                df.drivesDetail(
                    drives,
                    function (err, data) {
                        if (err) {
                            return console.log(err);
                        }
                        console.log(data);
                    }
                );
            }
        )


LICENSE
nodejs-disks - see License.md file
node-diskfree - see OriginalLicense.md file



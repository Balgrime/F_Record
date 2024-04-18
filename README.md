F_Record
A lightweight Photoshop plugin for recording the drawing process.
Plugin principle: call the interface of PS generator to capture process images when the canvas changes, and finally connect the images to generate a video.
Supported versions: PS 2019 and later (thanks to srylyx for helping with compatibility)
Supported systems: Windows, Mac (only Windows is temporarily available on GitHub)
Github: https://github.com/F-know/F_Record
Cloud drive download: https://pan.quark.cn/s/d3aaf46abc5e
Disclaimer: This plugin does not guarantee that it will work perfectly on any computer without bugs, so for important recording processes, please have a Plan B ready. Otherwise, I am not responsible for any losses incurred, after all, it's free. If you still have questions after reading all the content below, you can DM me on Bilibili (ID: F_know), and I will reply when I see it.
PS plugin development blog: https://uiscripting.com All the content of this plugin was completed step by step by following the blog of this great guy, taking one week.

Installation Method
If you have installed version 1.0 before, please delete 1.0 first. Do not split the same drawing process into two versions and record them separately.
If PS doesn't come with these paths, just create one yourself.

Windows
Place F_Record-CEP in /Adobe Photoshop/Required/CEP/extensions
Place F_Record-generator in /Adobe Photoshop/Plug-ins/Generator

Mac
Place F_Record-CEP in /Users/{username}/Library/Application Support/Adobe/CEP/extensions
Place F_Record-generator in /Adobe Photoshop/Plug-ins/Generator

Finally, open PS, edit-Preferences-Enable Generator (check), Load extension panels (check), restart PS, in the top column Window-Extensions you can find the plugin.

Introduction to plugin interface parameters
Path: Fill in the path for saving process images and outputting videos, not the installation location of the plugin. You can create a new folder anywhere and copy the path into it.
Saved image count: The number of process images saved. It will gradually increase as you proceed with the operation after starting recording.
Minimum save interval: Used to control the frequency of saving images, usually set to 0. If the canvas is large (e.g., over 5000*5000 pixels, depending on your computer performance), saving images will take longer, so the minimum save interval will be relatively large.
Recording duration: Used to control the time of the final output video, you can fill it in after recording, it is recommended to be within 5 minutes, which is directly related to the time it takes to generate the video (of course, if you don’t mind waiting a little longer, it’s also ok).

FAQ
Q: Plugin prompts "not correctly signed"?
A: Some files inside have been modified or damaged, try downloading it again, if it still doesn't work, you can search on Baidu, there are many solutions online.
Q: Installed according to the above tutorial, but the plugin was not found in the extensions?
A: Most likely, the location of the F_Record-CEP folder is wrong.
Q: After clicking start recording, it prompts "This path was not found"?
A: Make sure there are no quotation marks in the filled path information.
Q: After starting recording, the image count has always been zero?
A: Either the location of the F_Record-generator folder is incorrect, or the canvas is too large, and it saves slowly.
Q: Can I continue recording next time after closing PS?
A: Yes, remember to click continue recording.
Q: I don't want to draw this picture halfway through recording, how can I switch to another picture to record?
A: Just create a new folder with a new path, and switch back later if you want to draw again.
Q: Will cropping or expanding the canvas during recording affect the video?
A: The recording will adjust automatically.
Q: Will zooming, flipping, or rotating the canvas be recorded in the video?
A: Only changes to the view of the canvas, not the canvas itself, will not be recorded.
Q: When there are multiple canvases, which one will be recorded?
A: The one selected when clicking start recording.
Q: What affects the time it takes to output the video?
A: It mainly depends on the recording duration you set, and then it is also related to the number of images, but not related to the canvas size.
Q: Why does the output video stay at 0% all the time?
A: It may be because the recording duration is set too long. Or the number of images is too small, wait a little longer, and it will directly jump to 90%.
Q: Why does "undefined" error occur halfway through outputting the video?
A: Either you are using the first version and the canvas is very large, in which case you can only export the video in editing software like PR, or there are damaged images in your process images, such as when you closed PS halfway through saving a certain image (my guess), in this case, just find and delete the damaged image.

Unresolved Issues
Q: Not compatible with F_Record and some other plugins used at the same time?
A: Since I use very few other PS plugins, I don't know the reason for the time being.
Q: The plugin flashes and disappears after opening?
A: Currently, this problem seems to be related to some individual 2019 versions, I don't know why, but someone in the comment section said that downloading another PS solved the problem.
Q: Will the plugin record hidden layers?
A: Very few people will encounter this situation, the reason is also unknown, it is speculated that PS generator is damaged, you can also try downloading another PS.
Q: Will the video recorded have color deviation?
A: There is a little bit, I also found out from someone's reminder. I use ffmpeg to merge videos, but in color space conversion, but I don't know how to fix it yet.
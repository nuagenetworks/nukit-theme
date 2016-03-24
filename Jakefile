var ENV = require("system").env,
    FILE = require("file"),
    task = require("jake").task,
    FileList = require("jake").FileList,
    blend = require("cappuccino/jake").blend,
    configuration = ENV["CONFIG"] || ENV["CONFIGURATION"] || ENV["c"] || "Release";

blend ("NUFlat.blend", function(task)
{
    task.setBuildIntermediatesPath(FILE.join(ENV["CAPP_BUILD"], "NUFlat.build", configuration))
    task.setBuildPath(FILE.join(ENV["CAPP_BUILD"], configuration));

    task.setThemeDescriptors(new FileList("ThemeDescriptors.j"));
    task.setIdentifier("net.nuagenetworks.NUFlat");
    task.setResources(new FileList("Resources/*"));
});

task ("build", ["NUFlat.blend"]);

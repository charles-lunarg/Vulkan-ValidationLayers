<!-- markdownlint-disable MD041 -->
<!-- Copyright 2015-2019 LunarG, Inc. -->
[![Khronos Vulkan][1]][2]

[1]: https://vulkan.lunarg.com/img/Vulkan_100px_Dec16.png "https://www.khronos.org/vulkan/"
[2]: https://www.khronos.org/vulkan/

# Object Lifetimes Validation

[![Creative Commons][3]][4]

[3]: https://i.creativecommons.org/l/by-nd/4.0/88x31.png "Creative Commons License"
[4]: https://creativecommons.org/licenses/by-nd/4.0/

The object tracking validation object tracks all Vulkan objects. Object lifetimes are validated
along with issues related to unknown objects and object destruction and cleanup.

All Vulkan dispatchable and non-dispatchable objects are tracked by this module.

This layer validates that:

- only known objects are referenced and destroyed
- lookups are performed only on objects being tracked
- objects are correctly freed/destroyed

Validation will print errors if validation checks are not correctly met and warnings if improper
reference of objects is detected.

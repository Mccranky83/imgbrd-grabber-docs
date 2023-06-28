---
title: Library usage
---


## Library usage

### Introduction
Grabber can be used as a C++ library if necessary.

### Basic usage
```cpp
auto *profile = new Profile("path/to/dir"); // Directory containing the program's "settings.ini" file

auto *engine = new JavaScriptSourceEngine("model.js", "helper.js");
if (!engine->isValid()) {
    return;
}

auto *site = new Site("www.test.com", engine, "path/to/site", profile); // Directory containing the site's "settings.ini" file

site->login();
// wait for `Site::loggedIn` signal
```
---
title: "Specifying the Path to Profiling Tools Command Line Tools | Microsoft Docs"
ms.date: "11/04/2016"
ms.topic: "conceptual"
ms.assetid: 7047bf18-5779-4f6e-872c-66e2fc47c969
author: "mikejo5000"
ms.author: "mikejo"
manager: jillfra
monikerRange: 'vs-2017'
ms.workload:
  - "multiple"
---
# Specify the path to profiling tools command-line tools

The path of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profiling Tools command-line tools is not added to the PATH environment variable. On 32-bit computers, the tools are in a single directory. There are 32-bit and 64-bit versions of the profiling tools on 64-bit computers.

## 32-bit computers

::: moniker range="vs-2017"
 For native code, the Visual Studio profiler APIs are in *VSPerf.dll*. The header file, *VSPerf.h*, and the import library, *VSPerf.lib*, are located in the *Microsoft Visual Studio\2017\Team Tools\Performance Tools\PerfSDK* directory.
::: moniker-end

 For managed code, the profiler APIs are in the *Microsoft.VisualStudio.Profiler.dll*. This DLL is found in the *Microsoft Visual Studio\Shared\Common\VSPerfCollectionTools* directory.

## 64-bit computers

On 64-bit computers, specify the path according to the target platform of the profiled application.

::: moniker range="vs-2017"
- For 32-bit applications, the default profiler tools directory is:

     (native) *Microsoft Visual Studio\2017\Team Tools\Performance Tools\PerfSDK*
     (managed) *Microsoft Visual Studio\Shared\Common\VSPerfCollectionTools*

- For 64-bit applications, the default profiler tools directory is:

     (native) *Microsoft Visual Studio\2017\Team Tools\Performance Tools\x64\PerfSDK*
     (managed) *Microsoft Visual Studio\Shared\Common\VSPerfCollectionTools\x64*
::: moniker-end

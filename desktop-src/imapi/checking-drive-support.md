---
title: Проверка поддержки диска
description: В следующем примере изучаются характеристики устройства, которые не зависят от носителя, вставленного в устройство.
ms.assetid: 2d7e5ff9-7f1b-4bc1-bbc8-5e7eab45cdb0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49173ab8070821a03028106080dedc21925b088c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411404"
---
# <a name="checking-drive-support"></a><span data-ttu-id="63dd8-103">Проверка поддержки диска</span><span class="sxs-lookup"><span data-stu-id="63dd8-103">Checking Drive Support</span></span>

<span data-ttu-id="63dd8-104">В следующем примере изучаются характеристики устройства, которые не зависят от носителя, вставленного в устройство.</span><span class="sxs-lookup"><span data-stu-id="63dd8-104">The following example examines disc device characteristics that are independent of media inserted in the device.</span></span> <span data-ttu-id="63dd8-105">В частности, он извлекает списки поддерживаемых функций, поддерживаемых профилей и страниц поддерживаемых режимов, а также текущие параметры и профиль компонента.</span><span class="sxs-lookup"><span data-stu-id="63dd8-105">More specifically, it retrieves lists of supported features, supported profiles, and supported mode pages, as well as the current feature settings and profile.</span></span>


```VB
' This script examines the burn device characteristics such as 
' product ID, product revision level, feature set, and profiles. 

' Copyright (C) Microsoft Corp. 2006

Option Explicit

' Constants
const IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE = 47

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(Index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' *** - Formatting to display recorder info
    WScript.Echo "--------------------------------------------------"
    Wscript.Echo " ActiveRecorderId: " & recorder.ActiveDiscRecorder
    Wscript.Echo "        Vendor Id: " & recorder.VendorId
    Wscript.Echo "       Product Id: " & recorder.ProductId
    Wscript.Echo " Product Revision: " & recorder.ProductRevision
    Wscript.Echo "       VolumeName: " & recorder.VolumeName
    Wscript.Echo "   Can Load Media: " & recorder.DeviceCanLoadMedia
    Wscript.Echo "    Device Number: " & recorder.LegacyDeviceNumber

    Dim mountPoint
    For Each mountPoint In recorder.VolumePathNames
        WScript.Echo "      Mount Point: " & mountPoint
    Next

    WScript.Echo "Supported Features"  'in _IMAPI_FEATURE_PAGE_TYPE 
    Dim supportedFeature
    For Each supportedFeature  in recorder.SupportedFeaturePages
        if supportedFeature = _
            IMAPI_FEATURE_PAGE_TYPE_DVD_DASH_WRITE then
                WScript.Echo "    Feature: " & supportedFeature & _
                    "  Drive supports DVD-RW."
        else
                     WScript.Echo "    Feature: " & supportedFeature
        end if
    Next
    
    WScript.Echo "Current Features"    'in _IMAPI_FEATURE_PAGE_TYPE
    Dim currentFeature
    For Each currentFeature  in recorder.CurrentFeaturePages
        WScript.Echo "    Feature: " & currentFeature
    Next
    
    WScript.Echo "Supported Profiles"  'in _IMAPI_PROFILE_TYPE
    Dim supportedProfile
    For Each supportedProfile  in recorder.SupportedProfiles
        WScript.Echo "    Profile: " & supportedProfile
    Next

    WScript.Echo "Current Profiles"    'in _IMAPI_PROFILE_TYPE
    Dim currentProfile
    For Each currentProfile    in recorder.CurrentProfiles
        WScript.Echo "    Profile: " & currentProfile
    Next
    
    WScript.Echo "Supported Mode Pages"  'in  _IMAPI_MODE_PAGE_TYPE
    Dim supportedModePage       
    For Each supportedModePage in recorder.SupportedModePages
        WScript.Echo "    Mode Page: " & supportedModePage
    Next

    WScript.Echo
    WScript.Echo "----- Finished content -----"
    Main = 0
End Function
```



## <a name="related-topics"></a><span data-ttu-id="63dd8-106">См. также</span><span class="sxs-lookup"><span data-stu-id="63dd8-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63dd8-107">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="63dd8-107">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="63dd8-108">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="63dd8-108">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="63dd8-109">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="63dd8-109">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="63dd8-110">**\_ \_ тип страницы функции \_ IMAPI**</span><span class="sxs-lookup"><span data-stu-id="63dd8-110">**IMAPI\_FEATURE\_PAGE\_TYPE**</span></span>](/windows/desktop/api/imapi2/ne-imapi2-imapi_feature_page_type)
</dt> <dt>

[<span data-ttu-id="63dd8-111">**\_ \_ тип страницы режима \_ IMAPI**</span><span class="sxs-lookup"><span data-stu-id="63dd8-111">**IMAPI\_MODE\_PAGE\_TYPE**</span></span>](/windows/desktop/api/imapi2/ne-imapi2-imapi_mode_page_type)
</dt> <dt>

[<span data-ttu-id="63dd8-112">**\_Тип профиля \_ IMAPI**</span><span class="sxs-lookup"><span data-stu-id="63dd8-112">**IMAPI\_PROFILE\_TYPE**</span></span>](/windows/desktop/api/imapi2/ne-imapi2-imapi_profile_type)
</dt> </dl>

 

 





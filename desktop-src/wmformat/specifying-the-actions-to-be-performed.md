---
title: Указание действий для выполнения
description: Указание действий для выполнения
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Расширенный системный формат (ASF), указание действий
- ASF (Расширенный системный формат), указание действий
- Управление цифровыми правами (DRM), указание действий
- DRM (Управление цифровыми правами), указание действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412545"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="25316-107">Указание действий для выполнения</span><span class="sxs-lookup"><span data-stu-id="25316-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="25316-108">При первом вызове [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) для создания объекта Reader второй параметр представляет собой побитовое **или** значение [**ВМТ \_ прав**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="25316-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="25316-109">Используйте этот параметр, чтобы указать, какие действия приложение будет принимать в первом открываемом файле.</span><span class="sxs-lookup"><span data-stu-id="25316-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="25316-110">Эти действия непосредственно соответствуют правам, которые могут быть указаны в лицензии.</span><span class="sxs-lookup"><span data-stu-id="25316-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="25316-111">При последующих вызовах [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)можно изменить запрашиваемые права, вызвав [**Ивмдрмреадер:: сетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), указав определенную константу для свойства [**\_ Rights DRM**](drm-rights.md) и используя строковые литералы (типа **WCHAR**), разделенные точкой с запятой для определения прав.</span><span class="sxs-lookup"><span data-stu-id="25316-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="25316-112">В следующем фрагменте кода запрашиваются четыре права: Воспроизведите файл, скопируйте его на устройство и воспроизводите в составе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="25316-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="25316-113">Не путайте свойство [**\_ Rights DRM**](drm-rights.md) с свойством [**\_ flags DRM**](drm-flags.md) , которое является **DWORD** , используемым для указания прав, применяемых к локальной лицензии DRM версии 1 при копировании содержимого с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="25316-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="25316-114">См. также</span><span class="sxs-lookup"><span data-stu-id="25316-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25316-115">**Чтение защищенных файлов**</span><span class="sxs-lookup"><span data-stu-id="25316-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 





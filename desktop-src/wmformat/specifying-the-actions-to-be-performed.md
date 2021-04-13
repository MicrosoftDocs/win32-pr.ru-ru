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
# <a name="specifying-the-actions-to-be-performed"></a>Указание действий для выполнения

При первом вызове [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) для создания объекта Reader второй параметр представляет собой побитовое **или** значение [**ВМТ \_ прав**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) . Используйте этот параметр, чтобы указать, какие действия приложение будет принимать в первом открываемом файле. Эти действия непосредственно соответствуют правам, которые могут быть указаны в лицензии. При последующих вызовах [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)можно изменить запрашиваемые права, вызвав [**Ивмдрмреадер:: сетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), указав определенную константу для свойства [**\_ Rights DRM**](drm-rights.md) и используя строковые литералы (типа **WCHAR**), разделенные точкой с запятой для определения прав. В следующем фрагменте кода запрашиваются четыре права: Воспроизведите файл, скопируйте его на устройство и воспроизводите в составе списка воспроизведения.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Не путайте свойство [**\_ Rights DRM**](drm-rights.md) с свойством [**\_ flags DRM**](drm-flags.md) , которое является **DWORD** , используемым для указания прав, применяемых к локальной лицензии DRM версии 1 при копировании содержимого с компакт-диска.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Чтение защищенных файлов**](reading-protected-files.md)
</dt> </dl>

 

 





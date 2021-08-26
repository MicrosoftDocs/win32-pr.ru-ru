---
description: Указывает окно для механизма мультимедиа, применяемого для защиты выходных данных Protection Manager (ОПМ).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Атрибут MF_MEDIA_ENGINE_OPM_HWND (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1079e7b9503c73ea678e4f9fd3642ec94fe43a1326e6f33a635f81d1bc1a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013074"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>\_ \_ \_ Атрибут HWND ОПМ обработчика передачи мультимедиа MF \_

Указывает окно для механизма мультимедиа, применяемого для защиты [выходных данных Protection Manager](output-protection-manager.md) (ОПМ).

## <a name="data-type"></a>Тип данных

**HWND** хранится как **UINT64**

## <a name="remarks"></a>Remarks

Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.

Чтобы включить защиту ОПМ для воспроизведения видео, приложение должно выполнить одно из следующих действий:

-   При создании подсистемы мультимедиа задайте атрибут [ \_ \_ \_ \_ HWND для воспроизведения обработчика мультимедиа MF](mf-media-engine-playback-hwnd.md) .
-   Задайте \_ \_ атрибут HWND ОПМ Engine для обработчика мультимедиа \_ \_ при создании подсистемы мультимедиа.
-   Вызовите [**имфмедиаенгинепротектедконтент:: сетопмвиндов**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) в любой точке после создания обработчика мультимедиа, но до отображения защищенного содержимого.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты обработчика мультимедиа](media-engine-attributes.md)
</dt> </dl>

 

 





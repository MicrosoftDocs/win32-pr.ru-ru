---
description: Указывает окно для механизма мультимедиа, применяемого для защиты выходных данных Protection Manager (ОПМ).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Атрибут MF_MEDIA_ENGINE_OPM_HWND (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999889"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>\_ \_ \_ Атрибут HWND ОПМ обработчика передачи мультимедиа MF \_

Указывает окно для механизма мультимедиа, применяемого для защиты [выходных данных Protection Manager](output-protection-manager.md) (ОПМ).

## <a name="data-type"></a>Тип данных

**HWND** хранится как **UINT64**

## <a name="remarks"></a>Комментарии

Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.

Чтобы включить защиту ОПМ для воспроизведения видео, приложение должно выполнить одно из следующих действий:

-   При создании подсистемы мультимедиа задайте атрибут [ \_ \_ \_ \_ HWND для воспроизведения обработчика мультимедиа MF](mf-media-engine-playback-hwnd.md) .
-   Задайте \_ \_ атрибут HWND ОПМ Engine для обработчика мультимедиа \_ \_ при создании подсистемы мультимедиа.
-   Вызовите [**имфмедиаенгинепротектедконтент:: сетопмвиндов**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) в любой точке после создания обработчика мультимедиа, но до отображения защищенного содержимого.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                                |
| Header<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты обработчика мультимедиа](media-engine-attributes.md)
</dt> </dl>

 

 





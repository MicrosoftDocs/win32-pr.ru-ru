---
title: Сообщение WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: В \_ сообщении о \_ видеосаурцее WM Cap \_ появляется диалоговое окно, в котором пользователь может управлять источником видео.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- сообщение WM_CAP_DLG_VIDEOSOURCE Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f05d7e3dc421759229adffa4ecc4b78affc26f1b4244887b017614c2ab4d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803884"
---
# <a name="wm_cap_dlg_videosource-message"></a>\_ \_ Сообщение видеосаурце с диалогом WM Cap \_

В сообщении о **\_ \_ \_ видеосаурцее WM Cap** появляется диалоговое окно, в котором пользователь может управлять источником видео. Диалоговое окно Источник видео может содержать элементы управления, которые выбирают источники входных данных. изменение оттенка, контраста, яркости изображения; и изменить качество видео перед воспроизведением изображений в буфер кадров. Это сообщение можно отправить явно или с помощью макроса [**капдлгвидеосаурце**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Диалоговое окно Источник видео является уникальным для каждого драйвера записи. Некоторые драйверы записи могут не поддерживать диалоговое окно "источник видео". Приложения могут определить, поддерживает ли драйвер записи это сообщение, проверив элемент **фхасдлгвидеосаурце** структуры [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 






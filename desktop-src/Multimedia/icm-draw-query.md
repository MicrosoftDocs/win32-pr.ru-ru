---
title: Сообщение ICM_DRAW_QUERY (VFW. h)
description: Сообщение с \_ \_ запросом ICM Draw запрашивает драйвер подготовки к просмотру, чтобы определить, может ли он визуализировать данные в определенном формате. Это сообщение можно отправить явно или с помощью макроса Икдравкуери.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491148"
---
# <a name="icm_draw_query-message"></a>\_ \_ Сообщение запроса ICM Draw

Сообщение **с \_ \_ запросом ICM Draw** запрашивает драйвер подготовки к просмотру, чтобы определить, может ли он визуализировать данные в определенном формате. Это сообщение можно отправить явно или с помощью макроса [**икдравкуери**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*
</dt> <dd>

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если драйвер может отображать данные в указанном формате или ицерр \_ бадформат в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение отличается от [**ICM- \_ сообщений \_ Begin**](icm-draw-begin.md) , так как оно запрашивает драйвер в общем смысле. **ICM \_ \_Начало рисования** определяет, может ли драйвер выводить данные с использованием указанного формата в определенных условиях, таких как растяжение изображения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 


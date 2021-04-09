---
title: Сообщение ICM_DRAW_BEGIN (VFW. h)
description: '\_ \_ Сообщение о начале ICM Draw уведомляет драйвер подготовки, чтобы подготовиться к прорисовке данных.'
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989158"
---
# <a name="icm_draw_begin-message"></a>\_Сообщение начала прорисовки ICM \_

Сообщение **о \_ \_ начале ICM Draw** уведомляет драйвер подготовки, чтобы подготовиться к прорисовке данных.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*икдрвбгн*
</dt> <dd>

Указатель на структуру [**икдравбегин**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) , содержащую входной формат.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер **икдравбегин** в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает отображение данных на экране с указанными форматом или с кодом ошибки в противном случае. Возможные значения ошибок включают следующее.



| Значение               | Значение                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ИЦЕРР \_ бадформат    | Формат ввода или вывода не поддерживается.                                      |
| ИЦЕРР \_ NOTSUPPORTED | Драйвер не рисуется непосредственно на экране или не поддерживает это сообщение. |



 

## <a name="remarks"></a>Комментарии

Если требуется, чтобы драйвер распаковать данные в буфер, отправьте сообщение [**\_ \_ Begin распаковки**](icm-decompress-begin.md) .

**\_ \_ Начало** и [**\_ \_ конец**](icm-draw-end.md) изображения ICM не вложены в сообщения. Если драйвер получает функцию **ICM \_ Draw \_** , то перед **\_ \_ завершением** распаковки с использованием ICM Draw необходимо перезапустить распаковку с новыми параметрами.

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

 

 






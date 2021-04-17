---
title: Сообщение ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: Сообщение ICM \_ распаковка \_ Получение \_ палитры требует, чтобы драйвер распаковки видео предоставил таблицу цветов для выходной структуры битмапинфохеадер. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессжетпалетте.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672801"
---
# <a name="icm_decompress_get_palette-message"></a>ICM \_ распаковка \_ Получение \_ сообщения палитры

Сообщение **ICM \_ распаковка \_ Получение \_ палитры** требует, чтобы драйвер распаковки видео предоставил таблицу цветов для выходной структуры [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) . Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессжетпалетте**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*
</dt> <dd>

Указатель на структуру [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , содержащую входной формат.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*
</dt> <dd>

Указатель на структуру [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) , в которой будет содержаться таблица цветов. Пространство, зарезервированное для таблицы цветов, всегда имеет по крайней мере 256 цветов. Для этого параметра можно указать ноль, чтобы возвращался только размер таблицы цветов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Если *лпбиаутпут* имеет ненулевое значение, драйвер устанавливает для элемента **биклрусед** в [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)) число цветов в таблице цветов. Драйвер заполняет элемент **бмиколорс** в [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) на реальные цвета.

Драйвер должен поддерживать это сообщение только в том случае, если используется палитра, отличная от указанной во входном формате.

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

 


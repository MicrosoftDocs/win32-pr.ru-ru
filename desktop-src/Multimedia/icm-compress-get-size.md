---
title: Сообщение ICM_COMPRESS_GET_SIZE (VFW. h)
description: Сообщение ICM \_ \_ \_ Request Size получает запрос о том, что драйверу сжатия видео предоставлен максимальный размер одного кадра данных при сжатии в указанный формат вывода. Это сообщение можно отправить явно или с помощью макроса Иккомпрессжетсизе.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989161"
---
# <a name="icm_compress_get_size-message"></a>\_Сообщение о сжатии \_ получения \_ размера ICM

Сообщение **ICM Request \_ \_ \_ Size получает** запрос о том, что драйверу сжатия видео предоставлен максимальный размер одного кадра данных при сжатии в указанный формат вывода. Это сообщение можно отправить явно или с помощью макроса [**иккомпрессжетсизе**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*
</dt> <dd>

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую входной формат.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*лпбиаутпут*
</dt> <dd>

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает максимальное число байтов, которое может занимать один сжатый кадр.

## <a name="remarks"></a>Комментарии

Как правило, приложения отправляют это сообщение, чтобы определить размер буфера, выделяемого для сжатого кадра.

Драйвер должен вычислить размер максимально возможного кадра на основе входных и выходных форматов.

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

 


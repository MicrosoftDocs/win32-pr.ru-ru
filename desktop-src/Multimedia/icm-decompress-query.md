---
title: Сообщение ICM_DECOMPRESS_QUERY (VFW. h)
description: Сообщение с \_ запросом ICM распаковка \_ запрашивает драйвер распаковки видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может распаковать определенный входной формат в определенный выходной формат.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672800"
---
# <a name="icm_decompress_query-message"></a>\_Сообщение о распаковке \_ запроса ICM

Сообщение **с \_ \_ ЗАПРОСом ICM распаковка** запрашивает драйвер распаковки видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может распаковать определенный входной формат в определенный выходной формат. Это сообщение можно отправить явно или с помощью макроса [**икдекомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .


```C++
ICM_DECOMPRESS_QUERY 
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

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую выходной формат. Для этого параметра можно указать ноль, чтобы указать допустимый выходной формат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.

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

 


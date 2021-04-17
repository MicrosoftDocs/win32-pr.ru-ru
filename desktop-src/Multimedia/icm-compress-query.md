---
title: Сообщение ICM_COMPRESS_QUERY (VFW. h)
description: В \_ сообщении о \_ запросе сжатия ICM запрашивается драйвер сжатия видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может сжимать определенный входной формат в определенный выходной формат.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- ICM_COMPRESS_QUERY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672806"
---
# <a name="icm_compress_query-message"></a>\_Сообщение о \_ запросе сжатия ICM

В сообщении о **\_ \_ запросе сжатия ICM** запрашивается драйвер сжатия видео, чтобы определить, поддерживает ли он определенный входной формат, или же он может сжимать определенный входной формат в определенный выходной формат. Это сообщение можно отправить явно или с помощью макроса [**иккомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .


```C++
ICM_COMPRESS_QUERY 
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

Возвращает ИЦЕРР \_ ОК, если указанное сжатие поддерживается или ицерр \_ бадформат в противном случае.

## <a name="remarks"></a>Комментарии

Когда драйвер получает это сообщение, он должен проверить структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , связанную с *лпбиинпут* , чтобы определить, может ли он сжимать входной формат.

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

 


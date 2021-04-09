---
title: Сообщение ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: '\_ \_ \_ Сообщение о формате ICM uncompression получает запрос к выходному формату распакованных данных из драйвера распаковки видео. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессжетформат.'
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071896"
---
# <a name="icm_decompress_get_format-message"></a>Выводит \_ \_ сообщение о \_ форматировании ICM

Сообщение **о \_ \_ \_ формате ICM** uncompression получает запрос к выходному формату распакованных данных из драйвера распаковки видео. Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессжетформат**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
ICM_DECOMPRESS_GET_FORMAT 
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

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , в которой будет содержаться выходной формат. Можно указать ноль, чтобы запросить только размер выходного формата, как в макросе [**икдекомпрессжетформатсизе**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если *лпбиаутпут* равен нулю, возвращает размер структуры.

Если *лпбиаутпут* имеет ненулевое значение, функция ВОЗВРАЩАЕТ значение ицерр \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Если *лпбиаутпут* имеет ненулевое значение, драйвер должен заполнить структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) с выходным форматом по умолчанию, соответствующим формату входных данных, указанному для *лпбиинпут*. Если программа сжатия может создать несколько форматов, то форматом по умолчанию должен быть тот, который сохраняет максимальный объем информации.

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

 


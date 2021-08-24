---
title: Сообщение ICM_COMPRESS_BEGIN (VFW. h)
description: '\_ \_ Сообщение о начале сжатия ICM уведомляет драйвер сжатия видео о подготовке к сжатию данных. Это сообщение можно отправить явно или с помощью макроса Иккомпрессбегин.'
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- сообщение ICM_COMPRESS_BEGIN Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33a6ee9c080e2dfc7a779abd4ae2a788bbe136ddcab1ef529714639065553ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140952"
---
# <a name="icm_compress_begin-message"></a>\_ \_ Сообщение начала сжатия ICM

Сообщение **о \_ \_ начале сжатия ICM** уведомляет драйвер сжатия видео о подготовке к сжатию данных. Это сообщение можно отправить явно или с помощью макроса [**иккомпрессбегин**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .


```C++
ICM_COMPRESS_BEGIN 
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

Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает указанное сжатие или ицерр \_ бадформат, если формат входных или выходных данных не поддерживается.

## <a name="remarks"></a>Remarks

Драйвер должен выделять и инициализировать любые таблицы или память, необходимые для сжатия форматов данных при получении сообщения [**\_ сжатия ICM**](icm-compress.md) .

ВКМ сохраняет параметры последнего сообщения о **\_ \_ начале сжатия ICM** . Сообщения **о \_ начале сжатия ICM \_ Begin** и [**ICM \_ сжимать \_**](icm-compress-end.md) не вложены. Если драйвер получает коэффициент **\_ сжатия ICM \_** , прежде чем сжатие будет остановлено с **\_ \_ окончанием сжатия ICM**, необходимо перезапустить сжатие с новыми параметрами.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 


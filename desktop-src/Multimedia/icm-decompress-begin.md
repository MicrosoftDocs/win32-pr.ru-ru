---
title: Сообщение ICM_DECOMPRESS_BEGIN (VFW. h)
description: '\_ \_ Сообщение о начале распаковки ICM уведомляет драйвер о распаковке видео, чтобы подготовиться к распаковке данных. Это сообщение можно отправить явно или с помощью макроса Икдекомпрессбегин.'
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- сообщение ICM_DECOMPRESS_BEGIN Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d26a0ea99f089d558da639dfad99d4551237b180e595912973e0d22f634f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678354"
---
# <a name="icm_decompress_begin-message"></a>\_Сообщение начала распаковки ICM \_

Сообщение **о \_ \_ начале распаковки ICM** уведомляет драйвер о распаковке видео, чтобы подготовиться к распаковке данных. Это сообщение можно отправить явно или с помощью макроса [**икдекомпрессбегин**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .


```C++
ICM_DECOMPRESS_BEGIN 
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

Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.

## <a name="remarks"></a>Remarks

Когда драйвер получает это сообщение, он должен выделить буферы и выполнить все длительные операции, чтобы они могли эффективно обрабатывать [**\_ файлы ICM**](icm-decompress.md) .

Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение [**ICM \_ Draw**](icm-draw.md) .

Не вложены в сообщения End **\_ распаковки \_ Begin** и [**ICM \_ unуплотнение \_**](icm-decompress-end.md) . Если драйвер Получает подсистему **\_ распаковки ICM \_ Begin** до остановки распаковки **с \_ \_ окончанием распаковки ICM**, необходимо перезапустить распаковку с новыми параметрами.

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

 


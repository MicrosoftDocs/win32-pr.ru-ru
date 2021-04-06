---
title: Сообщение ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: Сообщение ICM \_ декомпрессекс \_ Begin уведомляет драйвер сжатия видео о подготовке к распаковке данных.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803365"
---
# <a name="icm_decompressex_begin-message"></a>\_Сообщение о \_ начале ICM декомпрессекс

Сообщение **ICM \_ декомпрессекс \_ Begin** уведомляет драйвер сжатия видео о подготовке к распаковке данных.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*икдекс*
</dt> <dd>

Указатель на структуру [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) , содержащую форматы входных и выходных данных.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если указанное распаковка поддерживается или ицерр \_ бадформат в противном случае.

## <a name="remarks"></a>Комментарии

Когда драйвер получает это сообщение, он должен выделить буферы и выполнить все длительные операции, чтобы они могли эффективно обрабатывать сообщения [**ICM \_ декомпрессекс**](icm-decompressex.md) .

Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение с помощью [**ICM \_ \_**](icm-draw-begin.md) .

[**\_ \_ Конечные**](icm-decompressex-end.md) сообщения **ICM \_ декомпрессекс \_ Begin** и ICM декомпрессекс не вложены. Если драйвер получает **ICM \_ декомпрессекс \_ Begin** до остановки распаковки с помощью **ICM \_ декомпрессекс \_ End**, он должен перезапустить распаковку с новыми параметрами.

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

 

 






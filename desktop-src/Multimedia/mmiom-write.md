---
title: Сообщение MMIOM_WRITE (Ммсистем. h)
description: Сообщение ММИОМ \_ Write отправляется в процедуру ввода-вывода с помощью функции ммиоврите, чтобы запросить запись данных в открытый файл.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989272"
---
# <a name="mmiom_write-message"></a>\_Сообщение записи ммиом

Сообщение **ммиом \_ Write** отправляется в процедуру ввода-вывода с помощью функции [**ммиоврите**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , чтобы запросить запись данных в открытый файл.


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*лпбуффер*
</dt> <dd>

Указатель на буфер, содержащий данные для записи в файл.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*кбврите*
</dt> <dd>

Число байтов для записи в файл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число байтов, фактически записанных в файл. Если возникает ошибка, возвращается значение 1.

## <a name="remarks"></a>Комментарии

Процедура ввода-вывода отвечает за обновление элемента **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) для отражения нового расположения файла после операции записи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



 


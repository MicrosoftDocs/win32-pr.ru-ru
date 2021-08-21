---
title: Сообщение MMIOM_WRITE (Ммсистем. h)
description: Сообщение ММИОМ \_ Write отправляется в процедуру ввода-вывода с помощью функции ммиоврите, чтобы запросить запись данных в открытый файл.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- сообщение MMIOM_WRITE Windows мультимедиа
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
ms.openlocfilehash: 755b89d7e268e266b4761142dc3820bdd4d33d4bd4d86522ce5363b95e5be282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065274"
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

## <a name="remarks"></a>Remarks

Процедура ввода-вывода отвечает за обновление элемента **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) для отражения нового расположения файла после операции записи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



 


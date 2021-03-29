---
title: Сообщение MMIOM_READ (Ммсистем. h)
description: Сообщение ММИОМ \_ readed отправляется в процедуру ввода-вывода с помощью функции ммиореад, чтобы запросить чтение указанного числа байтов из открытого файла.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493266"
---
# <a name="mmiom_read-message"></a>ММИОМ \_ Чтение сообщения

Сообщение **ммиом \_ readed** отправляется в процедуру ввода-вывода с помощью функции [**ммиореад**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) , чтобы запросить чтение указанного числа байтов из открытого файла.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*лбуффер*
</dt> <dd>

Указатель на буфер, который должен быть заполнен данными, считанными из файла.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*кбреад*
</dt> <dd>

Число байтов для чтения из файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число байтов, фактически считанных из файла. Если не удается прочитать больше байтов, возвращается значение 0. Если возникает ошибка, возвращается значение 1.

## <a name="remarks"></a>Комментарии

Процедура ввода-вывода отвечает за обновление элемента **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) для отражения нового расположения файла после операции чтения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



 


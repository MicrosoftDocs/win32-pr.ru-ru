---
title: Сообщение MMIOM_OPEN (Ммсистем. h)
description: Сообщение ММИОМ \_ Open отправляется в процедуру ввода-вывода с помощью функции ммиупен, чтобы запросить открытие или удаление файла.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650402"
---
# <a name="mmiom_open-message"></a>ММИОМ \_ открытое сообщение

Сообщение **ммиом \_ Open** отправляется в процедуру ввода-вывода с помощью функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) , чтобы запросить открытие или удаление файла.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*лпсзфиленаме*
</dt> <dd>

Строка, заканчивающаяся нулем и содержащая имя открываемого файла.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ММСИСЕРР \_ в случае успеха или ошибки в противном случае. Возможные значения ошибок включают следующее.



| Требование | Значение |
|--------------------|---------------------------------------------|
| ММИОМ \_ каннотопен  | Не удалось открыть файл.               |
| ММИОМ \_ OUTOFMEMORY | Недостаточно памяти для выполнения операции. |



 

## <a name="remarks"></a>Комментарии

Элемент **dwFlags** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) содержит флаги, передаваемые функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .

Элемент **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) инициализируется нулевым значением. Если это значение неверно, процедура ввода-вывода должна исправить ее.

Если приложение передавало структуру [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) в [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), возвращаемое значение возвращается в элементе **верроррет** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



 


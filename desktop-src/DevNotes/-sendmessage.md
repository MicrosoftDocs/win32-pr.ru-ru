---
description: Отправляет указанное сообщение в окно или в окна.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: Функция _SendMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648020"
---
# <a name="_sendmessage-function"></a>\_SendMessage, функция

\[Эта функция является оболочкой для функции **SendMessage** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать **SendMessage** напрямую.\]

Отправляет указанное сообщение в окно или в окна. См. раздел [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

## <a name="syntax"></a>Синтаксис


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 

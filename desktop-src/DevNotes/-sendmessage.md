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
ms.openlocfilehash: bdd8a072970d8e6fb5e9af082f6f220531539a1c0061a7688d48be30dd659a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572574"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 

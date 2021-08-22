---
description: Отправляет входящие отправленные сообщения, проверяет очередь сообщений потока на наличие отправленного сообщения и получает сообщение (если оно существует).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: Функция _PeekMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2a2fbfcf1903fcafba77227a6b2b9f51b9c6a45ef2e8a20f7482db1f3ec2a7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538894"
---
# <a name="_peekmessage-function"></a>\_Функция PeekMessage

\[Эта функция является оболочкой для функции **PeekMessage** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать **PeekMessage** напрямую.\]

Отправляет входящие отправленные сообщения, проверяет очередь сообщений потока на наличие отправленного сообщения и получает сообщение (если оно существует). См. [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

## <a name="syntax"></a>Синтаксис


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 

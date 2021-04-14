---
description: Возвращает имя пользователя.
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: Функция _GetUserName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648031"
---
# <a name="_getusername-function"></a>\_Функция UserName

\[Эта функция является оболочкой для функции- **имени пользователя** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать метод. **username** напрямую.\]

Возвращает имя пользователя. См. [**имя пользователя**](/windows/win32/api/winbase/nf-winbase-getusernamea).

## <a name="syntax"></a>Синтаксис


```C++
BOOL _GetUserName(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 

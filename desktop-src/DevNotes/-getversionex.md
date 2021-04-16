---
description: Возвращает сведения о версии операционной системы.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: Функция _GetVersionEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657020"
---
# <a name="_getversionex-function"></a>\_GetVersionEx, функция

\[Эта функция является оболочкой для функции **GetVersionEx** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать **GetVersionEx** напрямую.\]

Возвращает сведения о версии операционной системы. См. раздел [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).

## <a name="syntax"></a>Синтаксис


```C++
BOOL _GetVersionEx(
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

[**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 

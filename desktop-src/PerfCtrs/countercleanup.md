---
description: Удаляет регистрацию поставщиков.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Функция Каунтерклеануп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: fe06923849a12609b6662505df94c927c3d9dfd4aeb8bc6a42bd6a225e042ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011372"
---
# <a name="countercleanup-function"></a>Функция Каунтерклеануп

Удаляет регистрацию поставщика.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Поставщик вызывает эту функцию. Функция вызывает функцию [**перфстоппровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) для удаления регистрации поставщика.

Средство [**КТРПП**](ctrpp.md) создает эту встроенную функцию при указании аргумента **-o** . Имя функции включает строку *префикса* , если указан аргумент **-prefix** (например, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 





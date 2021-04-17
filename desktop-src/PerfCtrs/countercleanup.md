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
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663247"
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

## <a name="remarks"></a>Комментарии

Поставщик вызывает эту функцию. Функция вызывает функцию [**перфстоппровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) для удаления регистрации поставщика.

Средство [**КТРПП**](ctrpp.md) создает эту встроенную функцию при указании аргумента **-o** . Имя функции включает строку *префикса* , если указан аргумент **-prefix** (например, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





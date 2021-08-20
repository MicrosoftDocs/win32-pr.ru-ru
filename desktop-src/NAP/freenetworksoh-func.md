---
title: Функция Фринетворксох (Напутил. h)
description: Освобождает структуру данных Нетворксох.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- Фринетворксох функция NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c2d3db800860295e0fa6173422ffeec0ca144550cc3ddfdf8a1ea391b6c6eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134755"
---
# <a name="freenetworksoh-function"></a>Функция Фринетворксох

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фринетворксох** освобождает структуру данных [**нетворксох**](/windows/win32/api/naptypes/ns-naptypes-networksoh) .

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нетворксох* \[ окне\]
</dt> <dd>

Указатель на структуру данных [**нетворксох**](/windows/win32/api/naptypes/ns-naptypes-networksoh) для освобождения.

</dd> </dl>

## <a name="remarks"></a>Remarks

Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):

-   **Входные** параметры выделяются и освобождаются вызывающей стороной.
-   **Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.
-   **Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.

Все функции NAP для освобождения памяти также освобождают все внедренные указатели.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Напутил. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






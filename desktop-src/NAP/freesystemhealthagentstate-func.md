---
title: Функция Фрисистемхеалсажентстате (Напутил. h)
description: Освобождает структуру данных Системхеалсажентстате.
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- Фрисистемхеалсажентстате функция NAP
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce59135de1c8f47d84a07f01dbb5f2bbe697f9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135535"
---
# <a name="freesystemhealthagentstate-function"></a>Функция Фрисистемхеалсажентстате

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фрисистемхеалсажентстате** освобождает структуру данных [**системхеалсажентстате**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) .

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состояние* \[ окне\]
</dt> <dd>

Указатель на структуру данных [**системхеалсажентстате**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) для освобождения.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):

-   **Входные** параметры выделяются и освобождаются вызывающей стороной.
-   **Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.
-   **Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.

Все функции NAP для освобождения памяти также освобождают все внедренные указатели.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Напутил. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






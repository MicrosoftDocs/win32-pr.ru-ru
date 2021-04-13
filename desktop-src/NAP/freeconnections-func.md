---
title: Функция Фриконнектионс (Напутил. h)
description: Освобождает структуру данных соединений.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- Фриконнектионс функция NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340395"
---
# <a name="freeconnections-function"></a>Функция Фриконнектионс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фриконнектионс** освобождает структуру данных [**Connections**](connections-struct.md) .

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*подключения* \[ окне\]
</dt> <dd>

Указатель на структуру [**Connections**](connections-struct.md) для освобождения.

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аллокконнектионс**](allocconnections-func.md)
</dt> </dl>

 

 






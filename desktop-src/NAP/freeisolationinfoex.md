---
title: Функция Фриисолатионинфоекс (Напутил. h)
description: Освобождает структуру данных Исолатионинфоекс.
ms.assetid: 9ca0e5ae-aed9-43e9-b8f7-90f13d62ac16
keywords:
- Фриисолатионинфоекс функция NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfoEx
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9ee8e9fc8dc7cdfa9abf72bb738a3ebf4569e47ca4d0eecf21ee19600a1673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781204"
---
# <a name="freeisolationinfoex-function"></a>Функция Фриисолатионинфоекс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фриисолатионинфоекс** освобождает структуру данных [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreeIsolationInfoEx(
  _In_ IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*исолатионинфо* \[ окне\]
</dt> <dd>

Указатель на структуру данных [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) для освобождения.

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



 

 






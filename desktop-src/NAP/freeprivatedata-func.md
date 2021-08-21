---
title: Функция Фриприватедата (Напутил. h)
description: Освобождает структуру данных PrivateData.
ms.assetid: 94b3618e-224f-4801-94f3-2faa1a298ec0
keywords:
- Фриприватедата функция NAP
topic_type:
- apiref
api_name:
- FreePrivateData
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c760a22ef377bd8d198ea3b913c6062e90338218a187cb9dec3af457a8a02493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134620"
---
# <a name="freeprivatedata-function"></a>Функция Фриприватедата

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фриприватедата** освобождает структуру данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreePrivateData(
  _In_ PrivateData *privateData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*privateData* \[ окне\]
</dt> <dd>

Указатель на структуру данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) для освобождения.

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



 

 






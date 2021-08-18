---
title: Функция Фринапкомпонентрегистратионинфоаррай (Напутил. h)
description: Освобождает указанное число структур данных Напкомпонентрегистратионинфо из массива.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- Фринапкомпонентрегистратионинфоаррай функция NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d9d1aba35e7bf1ef332231836bd986b881f0e2dc995bc430075dfadf7bd482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940502"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a>Функция Фринапкомпонентрегистратионинфоаррай

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фринапкомпонентрегистратионинфоаррай** освобождает указанное число структур данных [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) из массива.

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*количество* \[ окне\]
</dt> <dd>

Количество [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) структур в *info* , которые должны быть свободны.

</dd> <dt>

*сведения о* \[ окне\]
</dt> <dd>

Указатель на массив структур данных [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , которые должны быть освобождены.

</dd> </dl>

## <a name="remarks"></a>Remarks

Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):

-   **Входные** параметры выделяются и освобождаются вызывающей стороной.
-   **Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.
-   **Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.

Все функции NAP для освобождения памяти также освобождают все внедренные указатели.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Напутил. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






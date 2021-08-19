---
title: Функция Фрификсупинфо (Напутил. h)
description: Освобождает структуру данных Фиксупинфо.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Фрификсупинфо функция NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c869123aadd5310a346dcf8e7a2184ec84f7e40500744cbaf610cbfc54db42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368874"
---
# <a name="freefixupinfo-function"></a>Функция Фрификсупинфо

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Функция **фрификсупинфо** освобождает структуру данных [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .

## <a name="syntax"></a>Синтаксис


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фиксупинфо* \[ окне\]
</dt> <dd>

Указатель на структуру данных [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) для освобождения.

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
| Header<br/>                   | <dl> <dt>Напутил. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аллокфиксупинфо**](allocfixupinfo-func.md)
</dt> </dl>

 

 






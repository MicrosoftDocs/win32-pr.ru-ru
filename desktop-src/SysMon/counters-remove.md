---
title: Метод Counters. Remove
description: Удаляет экземпляр Каунтеритем из коллекции.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Удалить метод Сисмон
- Remove Method Сисмон, класс Counters
- Counters Class Сисмон, Remove, метод
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77226d87c49fdfd2e9d8d26c2699bcb4606de29a21bf2bd20a12ad0b70d6daa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956656"
---
# <a name="countersremove-method"></a>Метод Counters. Remove

Удаляет экземпляр [**каунтеритем**](counteritem.md) из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Индекс объекта [**каунтеритем**](counteritem.md) , который необходимо удалить из коллекции. Индекс основан на единицах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="exceptions"></a>Исключения



| Тип исключения                                  | Условие                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | Указан недопустимый индекс. Значение Err. Number —???. |



 

## <a name="remarks"></a>Remarks

Чтобы удалить все счетчики из коллекции, можно вызвать [**системмонитор. Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**Системмонитор. Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 






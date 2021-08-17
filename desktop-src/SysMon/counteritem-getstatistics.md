---
title: Каунтеритем. метод Statistics
description: Возвращает среднее, максимальное и минимальное значения счетчика.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Метод Сисмон
- Метод Сисмон, класс Каунтеритем
- Каунтеритем Class Сисмон, метод Statistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea1be162d68bb02db4842a7140effe653231dcc5105c4bea3b557abb02beab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883780"
---
# <a name="counteritemgetstatistics-method"></a>Каунтеритем. метод Statistics

Возвращает среднее, максимальное и минимальное значения счетчика.

## <a name="syntax"></a>Синтаксис


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Максимальное число* \[ заполняет\]
</dt> <dd>

Максимальное значение счетчика.

</dd> <dt>

*минимальное* \[ заполняет\]
</dt> <dd>

Минимальное значение счетчика.

</dd> <dt>

*среднее значение* \[ заполняет\]
</dt> <dd>

Среднее значение счетчика.

</dd> <dt>

*состояние* \[ заполняет\]
</dt> <dd>

Указывает, являются ли значения допустимыми.



| Значение                                                                                              | Значение                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Допустимые значения.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Недопустимые значения.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Для вычисления статистических значений используются только те значения счетчика, которые видны в окне графа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каунтеритем**](counteritem.md)
</dt> <dt>

[**Каунтеритем. Жетдатаат**](counteritem-getdataat.md)
</dt> <dt>

[**Каунтеритем. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 






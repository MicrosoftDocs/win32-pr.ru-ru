---
title: Каунтеритем. Жетдатаат, метод
description: Извлекает указанное значение счетчика из определенной точки диаграммы.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Метод Жетдатаат Сисмон
- Метод Жетдатаат Сисмон, объект Каунтеритем
- Сисмон объекта Каунтеритем, метод Жетдатаат
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a02ec2b98fa75df138f8cd315c3464192e7714dc737c2b360e721085c8eebd77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957159"
---
# <a name="counteritemgetdataat-method"></a>Каунтеритем. Жетдатаат, метод

Извлекает указанное значение счетчика из определенной точки диаграммы.

## <a name="syntax"></a>Синтаксис


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс точки графа, значение которого необходимо получить. Допустимые значения находятся в диапазоне от 0 до ([**системмонитор. датапоинткаунт**](systemmonitor-datapointcount.md) -1).

</dd> <dt>

*который* \[ окне\]
</dt> <dd>

Тип значения счетчика, которое необходимо получить, например среднее значение счетчика, отображаемое в окне графа. Возможные значения см. в разделе [**сисмондататипе**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*вариант* \[ заполняет\]
</dt> <dd>

Полученное значение счетчика.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод следует использовать только в том случае, если

-   [**Системмонитор. дисплайтипе**](systemmonitor-displaytype.md) имеет значение сисмонлинеграф
-   [**Системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) имеет значение Сисмонлогфилес или сисмонскллог

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**каунтеритем**](counteritem.md)
</dt> <dt>

[**Каунтеритем. статистики**](counteritem-getstatistics.md)
</dt> <dt>

[**Каунтеритем. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 






---
description: '\_Константы побитового флага линекаллхубтраккинг описывают тип предоставляемого отслеживания концентратора вызовов.'
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Константы LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675455"
---
# <a name="linecallhubtracking_-constants"></a>\_Константы линекаллхубтраккинг

Константы побитового флага **линекаллхубтраккинг \_** описывают тип предоставляемого отслеживания концентратора вызовов.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**ЛИНЕКАЛЛХУБТРАККИНГ \_ аллкаллс**
</dt> <dd> <dl> <dt>



Отслеживание концентратора вызовов предоставляется на уровне вызовов.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**ЛИНЕКАЛЛХУБТРАККИНГ \_ None**
</dt> <dd> <dl> <dt>



Отслеживание концентратора вызовов не предоставляется.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**ЛИНЕКАЛЛХУБТРАККИНГ \_ провидерлевел**
</dt> <dd> <dl> <dt>



Концентраторы вызовов отправляются на уровне поставщика услуг. Не передаются сведения о вызове с помощью изменений вызова.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

Когда в этой структуре данных происходят изменения, в приложение отправляется сообщение [**Line \_ каллинфо**](line-callinfo.md) . Параметры этого сообщения являются маркером вызова и указанием измененного информационного элемента. Структура данных [**линекаллхубтраккингинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) указывает, какой тип отслеживания предоставляется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Строка \_ каллинфо**](line-callinfo.md)
</dt> <dt>

[**линекаллхубтраккингинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 





---
description: При переопределении в производном классе проверяет, соответствует ли указанный объект Иконтекстноде критериям.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Метод Иматческритериакаллбакк:: Евалуатеконтекстноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647159"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>Метод Иматческритериакаллбакк:: Евалуатеконтекстноде

При переопределении в производном классе проверяет, соответствует ли указанный объект [**иконтекстноде**](icontextnode.md) критериям.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекстнодетоевалуате* \[ окне\]
</dt> <dd>

Объект [**иконтекстноде**](icontextnode.md) для вычисления.

</dd> <dt>

*пбресулт* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если *пконтекстнодетоевалуате* соответствует критериям; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Чтобы использовать метод [**иинканализер:: финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md) или [**метод Иинканализер:: финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md), создайте класс, реализующий [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md). Реализуйте **иматческритериакаллбакк:: евалуатеконтекстноде** , чтобы вернуть **вариант \_ true** , если объект [**иконтекстноде**](icontextnode.md) соответствует Вашему критерию, и **вариант \_ false** в противном случае. Для некоторых критериев может потребоваться предоставить возможность инициализации или обслуживания состояния объекта **иматческритериакаллбакк** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иматческритериакаллбакк**](imatchescriteriacallback.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





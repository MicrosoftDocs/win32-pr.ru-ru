---
description: Изменяет текущий верхний альтернативный вариант на указанный альтернативный вариант и очищает тип подтверждения для всех объектов Иконтекстноде, связанных с альтернативой.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Метод Иинканализер:: Модифитопалтернате (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b35cda4534bc5c791e4815c584f6da5d9972c018283b6c9385f6bad998187505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092044"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>Метод Иинканализер:: Модифитопалтернате

Изменяет текущий верхний альтернативный вариант на указанный альтернативный вариант и очищает тип подтверждения для всех объектов [**иконтекстноде**](icontextnode.md) , связанных с альтернативой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*палтернате* \[ окне\]
</dt> <dd>

Объект [**ианалисисалтернате**](ianalysisalternate.md) , содержащий новый верхний альтернативный вариант.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Для получения вариантов анализа используйте метод [**иинканализер:: alternate**](iinkanalyzer-getalternates.md), [**Иинканализер:: Жеталтернатесфорконтекстнодес**](iinkanalyzer-getalternatesforcontextnodes.md)или [**метод иинканализер:: жеталтернатесфорстрокес**](iinkanalyzer-getalternatesforstrokes.md). Чтобы получить объекты [**иконтекстноде**](icontextnode.md) , связанные с альтернативным анализом, используйте [**метод Ианалисисалтернате:: жеталтернатенодес**](ianalysisalternate-getalternatenodes.md).

Чтобы изменить тип подтверждения для контекстного узла, используйте [**иконтекстноде:: Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**конфирматионтипе**](confirmationtype.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





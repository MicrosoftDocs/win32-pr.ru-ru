---
description: Удаляет указание анализа из Иинканализер.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: 'Иинканализер: метод:D Елетеаналисишинт (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6f514f20ed99f7fc56725f582b815639cb9d8b3179e9e428845d7e066b6e3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967293"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>Иинканализер: метод:D Елетеаналисишинт

Удаляет указание анализа из [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*финттоделете* \[ окне\]
</dt> <dd>

Указание по анализу из [**иинканализер**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Удаление подсказки анализа не помечает область подсказки для переанализа. Чтобы пометить область в подсказке для переанализа, используйте [**метод иинканализер:: сетдиртирегион**](iinkanalyzer-setdirtyregion.md) , чтобы задать для "грязной" области объединение текущей "грязной" области и области указания по анализу.

Указание удаляется из анализатора; Однако сам [**иконтекстноде**](icontextnode.md) не удаляется.

Этот метод возвращает код ошибки, если *финттоделете* является [**иконтекстноде**](icontextnode.md) , который не относится к типу Аналисишинт (см. [**иконтекстноде:: GetType**](icontextnode-gettype.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Креатеаналисишинт**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Метод Иинканализер:: Жетаналисишинтс**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Метод Иинканализер:: Жетаналисишинтсбинаме**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





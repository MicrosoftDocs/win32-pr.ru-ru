---
description: Извлекает подсказку анализа, вызвавшую это предупреждение.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Метод Ианалисисварнинг:: optimize (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940514"
---
# <a name="ianalysiswarninggethint-method"></a>Метод Ианалисисварнинг:: NOEXPAND

Извлекает подсказку анализа, вызвавшую это предупреждение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паналисишинт* \[ заполняет\]
</dt> <dd>

Узел контекста указания анализа, вызвавший это предупреждение, или **значение NULL** , если указание анализа не вызвало это предупреждение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *паналисишинт* , когда больше не нужно использовать узел контекста указания по анализу.

 

Примером указания по анализу, создающему [**ианалисисварнинг**](ianalysiswarning.md) , является указание анализа, которое содержит неверно написанный фактоид. В этом случае анализ рукописного ввода возвращает [**ианалисисстатус**](ianalysisstatus.md) , содержащий **ианалисисварнинг** , который ссылается на узел контекста указания по анализу с ошибкой фактоид. Кроме того, в этом случае метод [**ианалисисварнинг:: жетварнингкоде**](ianalysiswarning-getwarningcode.md) с предупреждением анализа возвращает значение [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) **аналисисварнингкоде \_ фактоиднотсуппортед**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ианалисисварнинг**](ianalysiswarning.md)
</dt> <dt>

[**ианалисисстатус**](ianalysisstatus.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 


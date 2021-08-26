---
description: Происходит перед тем, как Иинканализер согласовывает результаты анализа, чтобы приложение могла синхронизировать данные с Иинканализер.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Событие _IAnalysisProxyEvents:: Инканализерстатечангинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d4e32685e25e4c942b3c723df2152b1064bed59599fda54fcac00e22aab04206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884084"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Событие Ианалисиспроксевентс:: Инканализерстатечангинг

Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) согласовывает результаты анализа, чтобы приложение могла синхронизировать данные с **иинканализер**.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) , который собирается согласовать результаты анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Когда **иинканализер** вызывает это событие, приложение должно заполнить подузлы корневого узла анализатора красок (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) and [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md)).

[**Иинканализер**](iinkanalyzer.md) вызывает это событие после того, как оно вызывает событие [**\_ ианалисисевентс:: реадитореконЦиле**](-ianalysisevents-readytoreconcile.md) . Он вызывает это событие только при выполнении фонового анализа.

Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие **\_ ианалисиспроксевентс:: инканализерстатечангинг** . Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода. Разблокируйте структуру данных, когда **иинканализер** вызывает событие [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) или [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ианалисиспроксевентс**](-ianalysisproxyevents.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





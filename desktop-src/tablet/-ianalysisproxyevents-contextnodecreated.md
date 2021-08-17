---
description: Происходит после того, как Иинканализер создает объект Иконтекстноде.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Событие _IAnalysisProxyEvents:: Контекстнодекреатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5938ffda54542602248c5d04da0726d932b381aaff092f1c2038dd37ae4631e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675871"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Событие Ианалисиспроксевентс:: Контекстнодекреатед

Происходит после того, как [**иинканализер**](iinkanalyzer.md) создает объект [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) , создающий объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*пконтекстнодекреатед* \[ окне\]
</dt> <dd>

Новый объект [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализа рукописного ввода, создающий [**иконтекстноде**](icontextnode.md).

Когда [**иинканализер**](iinkanalyzer.md) создает [**Иконтекстноде**](icontextnode.md), новый **иконтекстноде** не содержит штрихов, не содержит ссылок на другие объекты **иконтекстноде** и может иметь не все заданные свойства. Кроме того, новый **иконтекстноде** добавляется в конец коллекции подузлов его родительского узла (см. раздел [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) and [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)). После этого события **иинканализер** может вызвать следующие события.

-   Событие [**\_ ианалисиспроксевентс:: строкерепарентед**](-ianalysisproxyevents-strokereparented.md) при перемещении штриха из одного контекстного узла в другой.
-   Событие [**\_ ианалисиспроксевентс:: контекстноделинкаддинг**](-ianalysisproxyevents-contextnodelinkadding.md) при добавлении [**иконтекстлинк**](icontextlink.md) в [**иконтекстноде**](icontextnode.md).
-   Событие [**\_ ианалисиспроксевентс:: контекстнодемовингтопоситион**](-ianalysisproxyevents-contextnodemovingtoposition.md) при изменении порядка [**иконтекстноде**](icontextnode.md) в коллекции подузлов его родительского узла.
-   [**Иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: контекстнодепропертиесупдатед**](-ianalysisproxyevents-contextnodepropertiesupdated.md) после того, как оно разрешит состояние [**иконтекстноде**](icontextnode.md) для этого этапа анализа.

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

 

 





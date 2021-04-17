---
description: Происходит перед тем, как Иинканализер перемещает объект Иконтекстноде в новую точку в коллекции подузлов родительского узла.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Событие _IAnalysisProxyEvents:: Контекстнодемовингтопоситион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703497"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Событие Ианалисиспроксевентс:: Контекстнодемовингтопоситион

Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) в новую точку в коллекции подузлов родительского узла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

Объект [**иинканализер**](iinkanalyzer.md) , перемещающий объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*писубнодетомове* \[ окне\]
</dt> <dd>

Перемещаемый объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*ппарентконтекстноде* \[ окне\]
</dt> <dd>

Родительский объект [**иконтекстноде**](icontextnode.md) объекта *писубнодетомове*.

</dd> <dt>

*улневиндекс* \[ окне\]
</dt> <dd>

Новое расположение *писубнодетомове* в коллекции подузлов родительского узла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализатора рукописного ввода, который перемещает [**иконтекстноде**](icontextnode.md) в коллекцию подузлов родительского узла (см. раздел [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) and [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
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

[**Иконтекстноде:: Жетпарентноде**](icontextnode-getparentnode.md)
</dt> <dt>

[**Иконтекстноде:: Жетсубнодес**](icontextnode-getsubnodes.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





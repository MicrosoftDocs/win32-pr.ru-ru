---
description: Происходит перед тем, как Иинканализер обращается к данным Stroke.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Событие _IAnalysisEvents:: Упдатестрокескаче (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a5854c8061a12dc558a2ca20ebd893880f899b2113065abd9b8122c53812aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047376"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Событие Ианалисисевентс:: Упдатестрокескаче

Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) обращается к данным Stroke.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидскаунт* \[ окне\]
</dt> <dd>

Число идентификаторов Stroke в *плстрокеидс*.

</dd> <dt>

*плстрокеидс* \[ окне\]
</dt> <dd>

Идентификаторы штрихов, данные пакетов которых были удалены.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

[**Иинканализер**](iinkanalyzer.md) вызывает это событие во время анализа рукописного ввода, когда он обращается к одному или нескольким штрихам, для которых данные пакета были удалены. Чтобы обновить данные пакета обводки, используйте метод [**метода иинканализер:: упдатестрокесдата**](iinkanalyzer-updatestrokesdata.md) .

[**Иинканализер**](iinkanalyzer.md) не вызывает это событие при доступе к частично заполненному конечному узлу рукописного ввода, если расположение узла не было задано параметром **иинканализер**.

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ианалисисевентс**](-ianalysisevents.md)
</dt> <dt>

[**\_ианалисиспроксевентс**](-ianalysisproxyevents.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Метод Иинканализер:: Упдатестрокесдата**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**Иконтекстноде:: Креатепартиаллипопулатедсубноде**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**Иконтекстноде:: Жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





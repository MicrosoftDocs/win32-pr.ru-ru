---
description: Указывает события, связанные с шагами анализа объекта Иинканализер.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Интерфейс _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2f49455e3e6fb68b2884cda380c304d7655b70d49ff338bcfb7c36904b449019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452169"
---
# <a name="_ianalysisevents-interface"></a>\_Интерфейс Ианалисисевентс

Указывает события, связанные с шагами анализа объекта [**иинканализер**](iinkanalyzer.md) .

-   [События](/windows)

### <a name="events"></a>События

Интерфейс **\_ ианалисисевентс** содержит следующие события.



| Событие                                                               | Описание                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Действие**](-ianalysisevents-activity.md)                       | Происходит при вызове метода [**иинканализер:: Analyze**](iinkanalyzer-analyze.md) или метода [**Иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md) .<br/> |
| [**интермедиатересултс**](-ianalysisevents-intermediateresults.md) | Происходит при завершении текущего промежуточного этапа анализа.<br/>                                                                                                                    |
| [**реадитореконЦиле**](-ianalysisevents-readytoreconcile.md)       | Происходит, когда [**иинканализер**](iinkanalyzer.md) готова к согласованию результатов своего фонового анализа с текущим состоянием.<br/>                                                  |
| [**Результаты**](-ianalysisevents-results.md)                         | Происходит после завершения заключительного этапа анализа.<br/>                                                                                                                                   |
| [**упдатестрокескаче**](-ianalysisevents-updatestrokescache.md)   | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) обращается к данным Stroke.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ианалисиспроксевентс**](-ianalysisproxyevents.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 


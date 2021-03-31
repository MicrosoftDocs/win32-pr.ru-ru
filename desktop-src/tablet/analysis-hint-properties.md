---
description: 'Определяет глобальные уникальные идентификаторы (GUID) для свойств узла указания по анализу (см. Иконтекстноде:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Свойства указания по анализу (Иагуид. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990825"
---
# <a name="analysis-hint-properties"></a>Свойства указания по анализу

Определяет глобальные уникальные идентификаторы (GUID) для свойств узла указания по анализу (см. [**иконтекстноде:: GetType**](icontextnode-gettype.md)).

В следующей таблице описаны сведения, на которые ссылается Каждая константа.



| Константа                                                                                                                                                                                                                                  | Описание                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ ахп \_ алловпартиалдиктионаритермс**</dt> </dl>       | Разрешены ли в подсказке анализа частичные словарные термины.<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ ахп \_ аналисишинтнаме**</dt> </dl>                                        | Имя подсказки анализа.<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ ахп \_ коерцетофактоид**</dt> </dl>                                           | Ограничивается ли анализатором рукописного ввода анализ рукописных данных в области подсказки для соответствия фактоид.<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ ахп \_ енабледуникодечарактерранжес**</dt> </dl> | Указание содержит массив символов, который представляет ограниченный набор поддерживаемых символов Юникода, поддерживаемый данным Инкрекогнизер.<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**GUID \_ ахп \_ фактоид**</dt> </dl>                                                                   | Фактоид в подсказке анализа.<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**\_ \_ руководство по ахп GUID**</dt> </dl>                                                                         | Структура [**инканалисисрекогнизергуиде**](inkanalysisrecognizerguide.md) , представляющая собой руководством для указания по анализу.<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ ахп \_ префикстекст**</dt> </dl>                                                          | Текст префикса для указания анализа.<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID \_ ахп \_ суффикстекст**</dt> </dl>                                                          | Текст суффикса в подсказке анализа.<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ ахп \_ топинкбреаксонли**</dt> </dl>                                        | Отключаются ли множественные сегменты в результатах распознавания рукописного ввода.<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**GUID \_ ахп \_ список слов**</dt> </dl>                                                                | Массив строк, представляющий список слов для указания анализа.<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID \_ ахп \_ вордмоде**</dt> </dl>                                                                | Определяет, следует ли анализатору рукописного ввода определять приоритеты отдельных слов по нескольким словам для указания анализа.<br/>                                      |



## <a name="remarks"></a>Комментарии

Эти идентификаторы GUID используются для указания свойств, которые [**иинканализер**](iinkanalyzer.md) может установить для узла контекста указания анализа (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md)).

Сведения о получении или задании свойств [**иконтекстноде**](icontextnode.md) в целом см. в разделе [Свойства узла контекста](context-node-properties.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                           |
| Header<br/>                   | <dl> <dt>Иагуид. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства узла контекста](context-node-properties.md)
</dt> <dt>

[Типы узлов контекста](context-node-types.md)
</dt> <dt>

[**Метод Иинканализер:: Креатеаналисишинт**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Метод Иинканализер:: Жетаналисишинтсбинаме**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[**Иконтекстноде:: Контаинспропертидата**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Жетпропертидатаидс**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Иконтекстноде:: Лоадпропертиесдата**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Иконтекстноде:: Ремовепропертидата**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Иконтекстноде:: Савепропертиесдата**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 





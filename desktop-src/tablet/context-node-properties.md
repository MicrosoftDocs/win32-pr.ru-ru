---
description: Определяет глобальные уникальные идентификаторы (GUID) для свойств Иконтекстноде.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Свойства узла контекста (Иагуид. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8eb1034516c62e2121f835951d1f04db5710d275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896538"
---
# <a name="context-node-properties"></a>Свойства узла контекста

Определяет глобальные уникальные идентификаторы (GUID) для свойств [**иконтекстноде**](icontextnode.md).

В следующей таблице описаны сведения, на которые ссылается Каждая константа.



| Константа                                                                                                                                                                                                 | Описание                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ КНП \_ алигнментлевел**</dt> </dl>             | Уровень выравнивания абзаца.<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**GUID \_ КНП \_ ascends**</dt> </dl>                            | Верхние края рукописного слова.<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**Базовый идентификатор GUID \_ КНП \_**</dt> </dl>                               | Базовая линия рукописного слова.<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ КНП \_ конфиденцелевел**</dt> </dl>          | Уровень достоверности в результатах распознавания.<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ КНП \_ кустомрекогнизерид**</dt> </dl> | Идентификатор пользовательского распознавателя рукописного ввода для узла пользовательского распознавателя.<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**GUID \_ КНП \_ нижние выносные**</dt> </dl>                         | Нижние края рукописного слова.<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**GUID \_ КНП \_ заполнение нажатием клавиши**</dt> </dl>                                  | Заполнение нажатием клавиши рукописного слова.<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ КНП \_ нодедата**</dt> </dl>                               | Данные изображения или текстовые данные изображения или текстового слова.<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ КНП \_ рекогнизедстринг**</dt> </dl>       | Распознанная строка.<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ КНП \_ ротатедбаундингбокс**</dt> </dl> | Повернутый ограничивающий прямоугольник.<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**GUID \_ КНП \_ семантиктипе**</dt> </dl>                   | Свойство содержит сведения о семантических типах, используемых при определении заметки, например о том, является ли она выноской, комментарием и т. д.<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ КНП \_ шапенаме**</dt> </dl>                            | Имя фигуры узла рукописного рисования.<br/>                                                                                                            |



## <a name="remarks"></a>Комментарии

Эти идентификаторы GUID используются для обнаружения свойств, которые [**иинканализер**](iinkanalyzer.md) может установить в [**иконтекстноде**](icontextnode.md). Анализатор рукописного ввода задает некоторые данные свойств на основе типа узла контекста (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)).

Сведения о получении или задании свойств, относящихся к узлам указания по анализу, см. в разделе [**Свойства указания анализа**](analysis-hint-properties.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                           |
| Header<br/>                   | <dl> <dt>Иагуид. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства указания по анализу](analysis-hint-properties.md)
</dt> <dt>

[Типы узлов контекста](context-node-types.md)
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

 

 





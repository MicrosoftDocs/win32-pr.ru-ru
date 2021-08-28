---
description: 'Дополнительные сведения: структура JET_TUPLELIMITS'
title: Структура JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc5a71328681e1ce415b1a34e9c8f718b460e7f0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471780"
---
# <a name="jet_tuplelimits-structure"></a>Структура JET_TUPLELIMITS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_tuplelimits-structure"></a>Структура JET_TUPLELIMITS

Структура **JET_TUPLELIMITS** позволяет настраивать характеристики индекса кортежа для каждого индекса, а не для каждого экземпляра, с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

**Windows Server 2003:** структура **JET_TUPLELIMITS** появилась в Windows Server 2003.

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>Элементы

**членгсмин**

Минимальная длина кортежа. Значение по умолчанию равно 3.

**членгсмакс**

Максимальная длина кортежа. Значение по умолчанию — 10.

**чтоиндексмакс**

Максимальная длина строки для индексирования. Например, если столбец имеет длину 100 символов, а **чтоиндексмакс** имеет значение 60, то будут индексироваться только первые 60 символов столбца. Значение по умолчанию — 32767.

**кчинкремент**

Это позволяет настроить шаг на основе каждого индекса.

**Windows Vista:** член **кчинкремент** появился в Windows Vista. до Windows Vista количество сдвигов окна («шаг») всегда было равно 1, как показано в примере в разделе «примечания».

**ичстарт**

Смещение в значении, с которого начинается извлечение кортежей из значения.

**Windows Vista:** член **ичстарт** появился в Windows Vista.

### <a name="remarks"></a>Комментарии

Индекс кортежа просматривает строку и индексирует все возможные подстроки **членгсмакс**. В конце строки (или в позиции **чтоиндексмакс** в зависимости от того, что происходит раньше), подстроки по меньшей мере **членгсмин** будут индексироваться.

Индекс кортежа можно использовать для поиска строк с подстановочными знаками в начале и в конце.

Если предположить, что строка с текстовым полем "дождя IN Испания \! " создается с параметрами **членгсмин**= 2, а **членгсмакс**= 3, в индексе создаются следующие записи:

ЧИАНГРАЙ  
ЗНАЧЕНИЯ ТИПАНА  
ОКНЕ  
"N I"  
ОКНЕ  
ОКНЕ  
"N S"  
ПОРТОВ  
SPA  
"Паи"  
ЗНАЧЕНИЯ ТИПАНА  
"В \! "  
"N \! "

Обратите внимание, что "IN" встречается дважды и что последняя запись ("N \! ") короче 3 (**членгсмакс**). Также обратите внимание, что алгоритм разбиения не знает о пробелах или словах и обрабатывает все символы одинаково.

**Windows xp:** Windows xp поддерживает индексы кортежей, но не имеет **JET_TUPLELIMITS**. Ядро СУБД будет использовать значения по умолчанию (**членгсмин**= 3, **членгсмакс**= 10, **чтоиндексмакс**= 32767). Эти значения по-прежнему можно изменить, но они задаются для каждого экземпляра с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)и [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)

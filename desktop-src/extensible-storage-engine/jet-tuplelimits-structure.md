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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999623"
---
# <a name="jet_tuplelimits-structure"></a>Структура JET_TUPLELIMITS


_**Применимо к:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>Структура JET_TUPLELIMITS

Структура **JET_TUPLELIMITS** позволяет настраивать характеристики индекса кортежа для каждого индекса, а не для каждого экземпляра, с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

**Windows Server 2003:** Структура **JET_TUPLELIMITS** появилась в Windows Server 2003.

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

**Windows Vista:** Член **кчинкремент** появился в Windows Vista. До Windows Vista объем смещения окна ("шаг") всегда равен 1, как показано в примере в разделе "Примечания".

**ичстарт**

Смещение в значении, с которого начинается извлечение кортежей из значения.

**Windows Vista:** Член **ичстарт** появился в Windows Vista.

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

**Windows XP:** Windows XP поддерживает индексы кортежей, но не имеет **JET_TUPLELIMITS**. Ядро СУБД будет использовать значения по умолчанию (**членгсмин**= 3, **членгсмакс**= 10, **чтоиндексмакс**= 32767). Эти значения по-прежнему можно изменить, но они задаются для каждого экземпляра с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)и [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)

---
description: 'Дополнительные сведения: параметры индекса'
title: Параметры индекса
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: f53430a6b624b6b65a5d02727dc16d7f1fba669d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470900"
---
# <a name="index-parameters"></a>Параметры индекса


_**Применимо к:** Windows | Windows Сервером_

## <a name="index-parameters"></a>Параметры индекса

Этот раздел содержит параметры, используемые для индекса.

*JET_paramIndexTupleIncrement*  
132  

Этот параметр задает значение по умолчанию для шага смещения, используемого для пошагового перехода к значению исходного столбца при создании каждого кортежа. Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .


| | | <p>Значение по умолчанию:</p> | <p>1</p> | | <p>Тип:</p> | <p>Целое число</p> | | <p>Допустимый диапазон:</p> | <p>0 - 32767</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>Windows Vista и более поздние версии</p> | 



*JET_paramIndexTupleStart*  
133  

Этот параметр задает значение по умолчанию для смещения в значении исходного столбца, с которого начнется создание кортежей. Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .


| | | <p>Значение по умолчанию:</p> | <p>0</p> | | <p>Тип:</p> | <p>Целое число</p> | | <p>Допустимый диапазон:</p> | <p>0 - 32767</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>Windows Vista и более поздние версии</p> | 



*JET_paramIndexTuplesLengthMax*  
111  

Этот параметр задает значение по умолчанию для максимальной длины кортежа в индексе кортежа. Дополнительные сведения см. в разделе Структура [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  до Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию. для Windows Vista это больше не поддерживается.


| | | <p>Значение по умолчанию:</p> | <p>10</p> | | <p>Тип:</p> | <p>Целое число</p> | | <p>Допустимый диапазон:</p> | <p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>Windows XP и более поздних версий</p> | 



*JET_paramIndexTuplesLengthMin*  
110  

Этот параметр задает значение по умолчанию для минимальной длины кортежа в индексе кортежа. Дополнительные сведения см. в разделе [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  до Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию. для Windows Vista это больше не поддерживается.


| | | <p>Значение по умолчанию:</p> | <p>3</p> | | <p>Тип:</p> | <p>Целое число</p> | | <p>Допустимый диапазон:</p> | <p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>Windows XP и более поздних версий</p> | 



*JET_paramIndexTuplesToIndexMax*  
112  

Этот параметр задает значение по умолчанию для максимальной длины исходной строки, которая должна быть разбита на кортежи для индекса кортежа. Дополнительные сведения см. в разделе [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  до Windows Vista установка этого параметра в нулевое значение применяет его к значению по умолчанию. для Windows Vista это больше не поддерживается.


| | | <p>Значение по умолчанию:</p> | <p>32767</p> | | <p>Тип:</p> | <p>Целое число</p> | | <p>Допустимый диапазон:</p> | <p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong> 0 – 32767</p><p><strong>Windows Vista:</strong> 1 – 32767</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>Windows XP и более поздних версий</p> | 



*JET_paramUnicodeIndexDefault*  
72  

Этот параметр управляет параметрами Юникода по умолчанию, используемыми любым индексом для ключевого столбца Юникода. Тип этого параметра — [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) и фактически передается с помощью указателя буфера, хранящегося в целочисленном параметре [жетжетсистемпараметер](./jetgetsystemparameter-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md). Размер буфера должен равняться размеру [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) и должен передаваться в [жетжетсистемпараметер](./jetgetsystemparameter-function.md) с помощью параметра размера буфера строки. Это явное несоответствие, но это поведение этого параметра.

Значение этого параметра по умолчанию содержит код языка для английского языка (США) и следующие флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa): LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.

**Windows 2000:**  СОРТИД в LCID игнорируется. Всегда используется СОРТИД SORT_DEFAULT.

**Windows 2000:**  Флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa) должны содержать следующие флаги: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH. Кроме того, флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa)могут содержать следующие флаги: NORM_IGNORENONSPACE.

**Примечание**  .  Если приложению требуется хранить данные в Юникоде, настоятельно рекомендуется не полагаться на параметры Юникода по умолчанию для индексов. Использование языка "Английский (США)" — запереть использования инвариантного языкового стандарта, и флаги [лкмапстрингв](/windows/win32/api/winnls/nf-winnls-lcmapstringa)по умолчанию могут серьезно мешать работе некоторых языков. Необходимо всегда указывать собственные параметры для параметров Юникода в JetCreateIndex2 с помощью [JET_INDEXCREATE](./jet-indexcreate-structure.md).


| | | <p>Значение по умолчанию:</p> | <p>Специальные функции</p> | | <p>Тип:</p> | <p>JET_UNICODEINDEX * (JET_UNICODEINDEX)</p> | | <p>Допустимый диапазон:</p> | <p>Специальные функции</p> | | <p>Область.</p> | <p>Экземпляр</p> | | <p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p> | <p>Да</p> | | <p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p> | <p>Нет</p> | | <p>Влияет на физический макет:</p> | <p>Нет</p> | | <p>Влияет на надежность:</p> | <p>Нет</p> | | <p>Влияет на производительность:</p> | <p>Нет</p> | | <p>Влияет на ресурсы:</p> | <p>Нет</p> | | <p>"Доступность":</p> | <p>Все</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетжетсистемпараметер](./jetgetsystemparameter-function.md)  
[жетинит](./jetinit-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)

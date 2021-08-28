---
description: 'Дополнительные сведения: структура JET_TABLECREATE'
title: Структура JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: fcc6c63b06614eb16379fbb18d59a5459a8e5085
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983037"
---
# <a name="jet_tablecreate-structure"></a>Структура JET_TABLECREATE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_tablecreate-structure"></a>Структура JET_TABLECREATE

Структура **JET_TABLECREATE** содержит сведения, необходимые для создания таблицы, заполненной столбцами и индексами в базе данных ESE. Структура **JET_TABLECREATE** используется [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер этой структуры в байтах (для будущего расширения). Он должен иметь значение sizeof (JET_TABLECREATE) в байтах.

**сзтабленаме**

Имя создаваемой таблицы.

Имя должно соответствовать следующим условиям:

  - Иметь значение меньше JET_cbNameMost, не включая завершающее значение NULL.

<!-- end list -->

  - Состоит из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), то есть символов ASCII 0x20, 0x22 через 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.

<!-- end list -->

  - Не должно начинаться с пробела.

<!-- end list -->

  - Состоит по крайней мере один символ, не являющийся пробелом.

**сзтемплатетабленаме**

Имя уже существующей таблицы, из которой наследуются базовые DDL (язык описания данных). Использование таблицы шаблонов позволяет легко создавать множество таблиц с одинаковыми столбцами и индексами.

**улпажес**

Начальное число страниц базы данных, выделяемых для таблицы. Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.

**улденсити**

Плотность таблицы в процентных точках. Число должно быть либо 0, либо находиться в диапазоне от 20 до 100. Передача значения 0 означает, что должно использоваться значение по умолчанию. Значение по умолчанию — 80.

**ргколумнкреате**

Массив структур [JET_COLUMNCREATE](./jet-columncreate-structure.md) , каждый из которых соответствует столбцу, создаваемому в новой таблице.

**кколумнс**

Число элементов [JET_COLUMNCREATE](./jet-columncreate-structure.md) в **ргколумнкреате**.

**ргиндекскреате**

Массив структур [JET_INDEXCREATE](./jet-indexcreate-structure.md) , каждый из которых соответствует индексу, создаваемому в новой таблице.

**Циндексес**

Число элементов [JET_INDEXCREATE](./jet-indexcreate-structure.md) в **ргиндекскреате**.

**грбит**

Группа битов, содержащая параметры для этого вызова, которые содержат ноль или более следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Параметр JET_bitTableCreateFixedDDL предотвращает выполнение DDL-операций в таблице (например, добавление или удаление столбцов).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Параметр JET_bitTableCreateTemplateTable приводит к тому, что таблица будет таблицей шаблонов. Новые таблицы могут затем указать имя этой таблицы в качестве таблицы шаблонов. Параметр JET_bitTableCreateTemplateTable подразумевает JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Не рекомендуется. Не используется.</p> | 



**TableID**

Поле вывода, которое содержит [JET_TABLEID](./jet-tableid.md) новой таблицы, если вызов API выполнен. Если вызов API завершается неудачей, значение не определено.

**ккреатед**

Поле вывода, содержащее количество объектов, созданных при успешности вызова API. Если вызов API завершается неудачей, значение не определено.

Количество создаваемых объектов равно сумме столбцов, таблиц и индексов, которые были успешно созданы.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_TABLECREATE_W</strong> (Юникод) и <strong>JET_TABLECREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[жеткреатетабле](./jetcreatetable-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)

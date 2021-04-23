---
description: 'Дополнительные сведения: структура JET_CONDITIONALCOLUMN'
title: Структура JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682964"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="a2086-103">Структура JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a2086-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="a2086-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a2086-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="a2086-105">Структура JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a2086-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="a2086-106">Структура **JET_CONDITIONALCOLUMN** определяет, как выполняется условное индексирование для данного индекса.</span><span class="sxs-lookup"><span data-stu-id="a2086-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="a2086-107">Условный индекс содержит элемент индекса только для тех строк, которые соответствуют заданному условию.</span><span class="sxs-lookup"><span data-stu-id="a2086-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="a2086-108">Однако условный столбец не является частью ключа индекса, он только управляет присутствием элемента индекса.</span><span class="sxs-lookup"><span data-stu-id="a2086-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="a2086-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="a2086-109">Members</span></span>

<span data-ttu-id="a2086-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="a2086-110">**cbStruct**</span></span>

<span data-ttu-id="a2086-111">Это поле должно быть инициализировано в sizeof (JET_CONDITIONALCOLUMN) в байтах.</span><span class="sxs-lookup"><span data-stu-id="a2086-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="a2086-112">**сзколумннаме**</span><span class="sxs-lookup"><span data-stu-id="a2086-112">**szColumnName**</span></span>

<span data-ttu-id="a2086-113">Имя столбца, содержащего данные, на которых ядро СУБД выполняет условное индексирование строки.</span><span class="sxs-lookup"><span data-stu-id="a2086-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="a2086-114">**грбит** Группа битов, которая предоставляет параметры для условного индекса.</span><span class="sxs-lookup"><span data-stu-id="a2086-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="a2086-115">Передача нулевых или логических значений (**или** ED) недопустима для **JET_CONDITIONALCOLUMN**.</span><span class="sxs-lookup"><span data-stu-id="a2086-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="a2086-116">Битовое поле должно быть ровно одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="a2086-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2086-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a2086-117">Value</span></span></p></th>
<th><p><span data-ttu-id="a2086-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a2086-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2086-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="a2086-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="a2086-120">Столбец, указанный параметром <em>сзколумннаме</em> , должен иметь значение NULL для записи индекса, чтобы данная строка отображалась в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="a2086-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2086-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="a2086-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="a2086-122">Столбец, указанный параметром <em>сзколумннаме</em> , должен иметь значение, отличное от NULL, для записи индекса, чтобы данная строка отображалась в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="a2086-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="a2086-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2086-123">Remarks</span></span>

<span data-ttu-id="a2086-124">Условный индекс содержит элемент индекса только для тех строк, которые соответствуют заданному условию.</span><span class="sxs-lookup"><span data-stu-id="a2086-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="a2086-125">Например, столбец может называться "помечен", а если строка помечена, в столбце задается значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="a2086-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="a2086-126">В JET_bitIndexColumnMustBeNonNull условном индексе этого столбца будут показаны все отмеченные строки, а в условном индексе JET_bitIndexColumnMustBeNull будут показаны непомеченные строки.</span><span class="sxs-lookup"><span data-stu-id="a2086-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="a2086-127">Это также удобный способ для удаления флагов и сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="a2086-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="a2086-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a2086-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2086-129"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a2086-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a2086-130">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a2086-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2086-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a2086-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a2086-132">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a2086-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2086-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a2086-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a2086-134">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a2086-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2086-135"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="a2086-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a2086-136">Реализуется как <strong>JET_CONDITIONALCOLUMN_W</strong> (Юникод) и <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a2086-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a2086-137">См. также:</span><span class="sxs-lookup"><span data-stu-id="a2086-137">See Also</span></span>

[<span data-ttu-id="a2086-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a2086-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a2086-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="a2086-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)

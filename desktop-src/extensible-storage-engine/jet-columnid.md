---
description: 'Дополнительные сведения: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896730"
---
# <a name="jet_columnid"></a><span data-ttu-id="b978b-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="b978b-103">JET_COLUMNID</span></span>


<span data-ttu-id="b978b-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b978b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="b978b-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="b978b-105">JET_COLUMNID</span></span>

<span data-ttu-id="b978b-106">Тип данных **JET_COLUMNID** определяет столбец в таблице.</span><span class="sxs-lookup"><span data-stu-id="b978b-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="b978b-107">Типы данных</span><span class="sxs-lookup"><span data-stu-id="b978b-107">Data Types</span></span>

<span data-ttu-id="b978b-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="b978b-108">JET_COLUMNID</span></span>

<span data-ttu-id="b978b-109">Определяет столбец в таблице.</span><span class="sxs-lookup"><span data-stu-id="b978b-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="b978b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b978b-110">Remarks</span></span>

<span data-ttu-id="b978b-111">Идентификаторы столбцов уникальны в пределах одной таблицы.</span><span class="sxs-lookup"><span data-stu-id="b978b-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="b978b-112">Когда известно, что столбец имеет определенный идентификатор столбца, он всегда будет иметь идентификатор столбца.</span><span class="sxs-lookup"><span data-stu-id="b978b-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="b978b-113">При восстановлении из резервной копии не изменится значение идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="b978b-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="b978b-114">Однако при удалении одного или нескольких столбцов таблицы, предшествовавших определенному столбцу таблицы, база данных Compact может изменить значение идентификатора столбца.</span><span class="sxs-lookup"><span data-stu-id="b978b-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="b978b-115">В некоторых случаях идентификаторы столбцов являются единственным средством идентификации столбцов.</span><span class="sxs-lookup"><span data-stu-id="b978b-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="b978b-116">При создании временной таблицы ее столбцы не имеют имен, но массив идентификаторов столбцов возвращается функцией Create.</span><span class="sxs-lookup"><span data-stu-id="b978b-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="b978b-117">Столбцы в разных таблицах могут иметь один и тот же идентификатор столбца.</span><span class="sxs-lookup"><span data-stu-id="b978b-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="b978b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b978b-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b978b-119"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="b978b-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b978b-120">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b978b-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b978b-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b978b-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b978b-122">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b978b-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b978b-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b978b-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b978b-124">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b978b-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


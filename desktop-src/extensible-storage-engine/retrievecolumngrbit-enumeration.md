---
description: Дополнительные сведения о перечислении Ретриевеколумнгрбит
title: Перечисление Ретриевеколумнгрбит
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683581"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="8a855-103">Перечисление Ретриевеколумнгрбит</span><span class="sxs-lookup"><span data-stu-id="8a855-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="8a855-104">Параметры для Жетретриевеколумн.</span><span class="sxs-lookup"><span data-stu-id="8a855-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="8a855-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="8a855-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8a855-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8a855-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8a855-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8a855-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8a855-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a855-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="8a855-109">Члены</span><span class="sxs-lookup"><span data-stu-id="8a855-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8a855-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="8a855-110">Member name</span></span></th>
<th><span data-ttu-id="8a855-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8a855-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8a855-112">Нет</span><span class="sxs-lookup"><span data-stu-id="8a855-112">None</span></span></td>
<td><span data-ttu-id="8a855-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a855-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8a855-114">ретриевекопи</span><span class="sxs-lookup"><span data-stu-id="8a855-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="8a855-115">Этот флаг заставляет столбец извлечь измененное значение, а не исходное значение.</span><span class="sxs-lookup"><span data-stu-id="8a855-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="8a855-116">Если значение не было изменено, то извлекается исходное значение.</span><span class="sxs-lookup"><span data-stu-id="8a855-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="8a855-117">Таким образом, значение, которое еще не было вставлено или Обновлено, может быть получено во время операции вставки или обновления записи.</span><span class="sxs-lookup"><span data-stu-id="8a855-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8a855-118">ретриевефроминдекс</span><span class="sxs-lookup"><span data-stu-id="8a855-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="8a855-119">Этот параметр используется для извлечения значений столбцов из индекса, если это возможно, без обращения к записи.</span><span class="sxs-lookup"><span data-stu-id="8a855-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="8a855-120">Таким образом, необязательная Загрузка записей может быть продолжена, если нужные данные будут доступны из самих записей индекса.</span><span class="sxs-lookup"><span data-stu-id="8a855-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8a855-121">ретриевефромпримарибукмарк</span><span class="sxs-lookup"><span data-stu-id="8a855-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="8a855-122">Этот параметр используется для извлечения значений столбцов из закладки индекса и может отличаться от значения индекса, если столбец отображается как в первичном, так и в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="8a855-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="8a855-123">Этот параметр не следует указывать, если текущий индекс является кластеризованным или первичным индексом.</span><span class="sxs-lookup"><span data-stu-id="8a855-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="8a855-124">Этот бит не может быть установлен, если также задан параметр Ретриевефроминдекс.</span><span class="sxs-lookup"><span data-stu-id="8a855-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8a855-125">ретриеветаг</span><span class="sxs-lookup"><span data-stu-id="8a855-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="8a855-126">Этот параметр используется для получения порядкового номера значения столбца с несколькими значениями в JET_RETINFO. Итагсекуенце.</span><span class="sxs-lookup"><span data-stu-id="8a855-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="8a855-127">Получение порядкового номера может быть дорогостоящей операцией, и ее следует выполнять только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8a855-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8a855-128">ретриевенулл</span><span class="sxs-lookup"><span data-stu-id="8a855-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="8a855-129">Этот параметр используется для извлечения значений NULL в столбцах с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="8a855-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="8a855-130">Если этот параметр не указан, значения NULL в столбцах с несколькими значениями будут пропускаться автоматически.</span><span class="sxs-lookup"><span data-stu-id="8a855-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8a855-131">ретриевеигноредефаулт</span><span class="sxs-lookup"><span data-stu-id="8a855-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="8a855-132">Этот параметр влияет только на столбцы с несколькими значениями и приводит к возвращению значения NULL, если запрошенный порядковый номер равен 1, а значения для столбца в записи не заданы.</span><span class="sxs-lookup"><span data-stu-id="8a855-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8a855-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a855-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8a855-134">Справочник</span><span class="sxs-lookup"><span data-stu-id="8a855-134">Reference</span></span>

[<span data-ttu-id="8a855-135">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8a855-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

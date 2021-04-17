---
description: Дополнительные сведения о перечислении Жетрекордсизегрбит
title: Перечисление Жетрекордсизегрбит
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662695"
---
# <a name="getrecordsizegrbit-enumeration"></a><span data-ttu-id="03e88-103">Перечисление Жетрекордсизегрбит</span><span class="sxs-lookup"><span data-stu-id="03e88-103">GetRecordSizeGrbit enumeration</span></span>

<span data-ttu-id="03e88-104">Параметры для [жетжетрекордсизе (JET_SESID, JET_TABLEID, JET_RECSIZE, жетрекордсизегрбит)](./vistaapi.jetgetrecordsize-method.md).</span><span class="sxs-lookup"><span data-stu-id="03e88-104">Options for [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md).</span></span>

<span data-ttu-id="03e88-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="03e88-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="03e88-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="03e88-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="03e88-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="03e88-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="03e88-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03e88-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
```

## <a name="members"></a><span data-ttu-id="03e88-109">Члены</span><span class="sxs-lookup"><span data-stu-id="03e88-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="03e88-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="03e88-110">Member name</span></span></th>
<th><span data-ttu-id="03e88-111">Описание</span><span class="sxs-lookup"><span data-stu-id="03e88-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="03e88-112">Нет</span><span class="sxs-lookup"><span data-stu-id="03e88-112">None</span></span></td>
<td><span data-ttu-id="03e88-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="03e88-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="03e88-114">инкопибуффер</span><span class="sxs-lookup"><span data-stu-id="03e88-114">InCopyBuffer</span></span></td>
<td><span data-ttu-id="03e88-115">Получение размера записи в буфере копирования, подготовленном или обновлении.</span><span class="sxs-lookup"><span data-stu-id="03e88-115">Retrieve the size of the record that is in the copy buffer prepared or update.</span></span> <span data-ttu-id="03e88-116">В противном случае TableID должно быть позиционировано на запись, а эта запись будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="03e88-116">Otherwise, the tableid must be positioned on a record, and that record will be used.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="03e88-117">руннингтотал</span><span class="sxs-lookup"><span data-stu-id="03e88-117">RunningTotal</span></span></td>
<td><span data-ttu-id="03e88-118">Перед заполнением содержимого JET_RECSIZE не обнуляются, эффективно выполняя сбор статистики по нескольким просмотренным или обновленным записям.</span><span class="sxs-lookup"><span data-stu-id="03e88-118">The JET_RECSIZE is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="03e88-119">Локальная</span><span class="sxs-lookup"><span data-stu-id="03e88-119">Local</span></span></td>
<td><span data-ttu-id="03e88-120">Пропускать невнутренние значения long.</span><span class="sxs-lookup"><span data-stu-id="03e88-120">Ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="03e88-121">Будет использоваться только локальная запись на странице.</span><span class="sxs-lookup"><span data-stu-id="03e88-121">Only the local record on the page will be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="03e88-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03e88-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="03e88-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="03e88-123">Reference</span></span>

[<span data-ttu-id="03e88-124">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="03e88-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

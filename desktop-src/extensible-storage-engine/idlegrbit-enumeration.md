---
description: Дополнительные сведения о перечислении Идлегрбит
title: Перечисление Идлегрбит
TOCTitle: IdleGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IdleGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.idlegrbit(v=EXCHG.10)
ms:contentKeyID: 39514282
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f02937241066762b6d711d89e62e67cfed9f41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263535"
---
# <a name="idlegrbit-enumeration"></a><span data-ttu-id="56b12-103">Перечисление Идлегрбит</span><span class="sxs-lookup"><span data-stu-id="56b12-103">IdleGrbit enumeration</span></span>

<span data-ttu-id="56b12-104">Параметры для [жетидле (JET_SESID, идлегрбит)](./api.jetidle-method.md).</span><span class="sxs-lookup"><span data-stu-id="56b12-104">Options for [JetIdle(JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span></span>

<span data-ttu-id="56b12-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="56b12-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="56b12-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56b12-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56b12-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56b12-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56b12-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56b12-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IdleGrbit
'Usage
Dim instance As IdleGrbit
```

``` csharp
[FlagsAttribute]
public enum IdleGrbit
```

## <a name="members"></a><span data-ttu-id="56b12-109">Члены</span><span class="sxs-lookup"><span data-stu-id="56b12-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="56b12-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="56b12-110">Member name</span></span></th>
<th><span data-ttu-id="56b12-111">Описание</span><span class="sxs-lookup"><span data-stu-id="56b12-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56b12-112">Нет</span><span class="sxs-lookup"><span data-stu-id="56b12-112">None</span></span></td>
<td><span data-ttu-id="56b12-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56b12-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56b12-114">флушбуфферс</span><span class="sxs-lookup"><span data-stu-id="56b12-114">FlushBuffers</span></span></td>
<td><span data-ttu-id="56b12-115">Запускает очистку хранилища версий.</span><span class="sxs-lookup"><span data-stu-id="56b12-115">Triggers cleanup of the version store.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="56b12-116">Компактный</span><span class="sxs-lookup"><span data-stu-id="56b12-116">Compact</span></span></td>
<td><span data-ttu-id="56b12-117">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="56b12-117">Reserved for future use.</span></span> <span data-ttu-id="56b12-118">Если этот флаг указан, API возвратит <a href="hh564840(v=exchg.10).md">инвалидгрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="56b12-118">If this flag is specified, the API will return <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="56b12-119">GetStatus</span><span class="sxs-lookup"><span data-stu-id="56b12-119">GetStatus</span></span></td>
<td><span data-ttu-id="56b12-120">Возвращает <a href="hh557250(v=exchg.10).md">идлефулл</a> , если хранилище версий больше половины места.</span><span class="sxs-lookup"><span data-stu-id="56b12-120">Returns <a href="hh557250(v=exchg.10).md">IdleFull</a> if version store is more than half full.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="56b12-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56b12-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56b12-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="56b12-122">Reference</span></span>

[<span data-ttu-id="56b12-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="56b12-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

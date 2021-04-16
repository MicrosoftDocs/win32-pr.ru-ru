---
description: Дополнительные сведения о перечислении Упдатегрбит
title: Перечисление Упдатегрбит (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542415"
---
# <a name="updategrbit-enumeration"></a><span data-ttu-id="317ac-103">Перечисление Упдатегрбит</span><span class="sxs-lookup"><span data-stu-id="317ac-103">UpdateGrbit enumeration</span></span>

<span data-ttu-id="317ac-104">Параметры для [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, упдатегрбит)](./server2003api.jetupdate2-method.md).</span><span class="sxs-lookup"><span data-stu-id="317ac-104">Options for [JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span></span>

<span data-ttu-id="317ac-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="317ac-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="317ac-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="317ac-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="317ac-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="317ac-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="317ac-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="317ac-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a><span data-ttu-id="317ac-109">Члены</span><span class="sxs-lookup"><span data-stu-id="317ac-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="317ac-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="317ac-110">Member name</span></span></th>
<th><span data-ttu-id="317ac-111">Описание</span><span class="sxs-lookup"><span data-stu-id="317ac-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="317ac-112">Нет</span><span class="sxs-lookup"><span data-stu-id="317ac-112">None</span></span></td>
<td><span data-ttu-id="317ac-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="317ac-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="317ac-114">CheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="317ac-114">CheckESE97Compatibility</span></span></td>
<td><span data-ttu-id="317ac-115"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="317ac-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="317ac-116">Этот флаг приводит к тому, что обновление возвращает ошибку, если в версии ESE для Windows 2000 не было возможно, что применяет меньшее максимальное число экземпляров столбцов с несколькими значениями в каждой записи, чем в более поздних версиях ESE.</span><span class="sxs-lookup"><span data-stu-id="317ac-116">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="317ac-117">Это важно только для приложений, которые хотят реплицировать данные между приложениями, размещенными в Windows 2000, и приложениями, размещенными в Windows 2003 или более поздних версиях ESE.</span><span class="sxs-lookup"><span data-stu-id="317ac-117">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows 2003, or later versions of ESE.</span></span> <span data-ttu-id="317ac-118">Это не должно быть необходимо для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="317ac-118">It should not be necessary for most applications.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="317ac-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="317ac-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="317ac-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="317ac-120">Reference</span></span>

[<span data-ttu-id="317ac-121">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="317ac-121">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

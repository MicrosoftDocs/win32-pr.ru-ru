---
description: Дополнительные сведения о перечислении Ендекстерналбаккупгрбит
title: Перечисление Ендекстерналбаккупгрбит
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272719"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="0b46d-103">Перечисление Ендекстерналбаккупгрбит</span><span class="sxs-lookup"><span data-stu-id="0b46d-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="0b46d-104">Параметры для [жетендекстерналбаккупинстанце (JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b46d-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="0b46d-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="0b46d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0b46d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b46d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b46d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b46d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b46d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b46d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="0b46d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0b46d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0b46d-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="0b46d-110">Member name</span></span></th>
<th><span data-ttu-id="0b46d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0b46d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0b46d-112">Нет</span><span class="sxs-lookup"><span data-stu-id="0b46d-112">None</span></span></td>
<td><span data-ttu-id="0b46d-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b46d-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0b46d-114">Норм.</span><span class="sxs-lookup"><span data-stu-id="0b46d-114">Normal</span></span></td>
<td><span data-ttu-id="0b46d-115">Клиентское приложение полностью завершило резервное копирование и завершается нормально.</span><span class="sxs-lookup"><span data-stu-id="0b46d-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0b46d-116">Прервать</span><span class="sxs-lookup"><span data-stu-id="0b46d-116">Abort</span></span></td>
<td><span data-ttu-id="0b46d-117">Клиентское приложение прерывает резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="0b46d-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0b46d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b46d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b46d-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="0b46d-119">Reference</span></span>

[<span data-ttu-id="0b46d-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0b46d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

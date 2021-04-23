---
description: 'Дополнительные сведения: перечисление JET_SNT'
title: Перечисление JET_SNT
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710881"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="7521c-103">Перечисление JET_SNT</span><span class="sxs-lookup"><span data-stu-id="7521c-103">JET_SNT enumeration</span></span>

<span data-ttu-id="7521c-104">Тип отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="7521c-104">Type of progress being reported.</span></span>

<span data-ttu-id="7521c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7521c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7521c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7521c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7521c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7521c-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="7521c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7521c-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7521c-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="7521c-109">Member name</span></span></th>
<th><span data-ttu-id="7521c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7521c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7521c-111">Начать</span><span class="sxs-lookup"><span data-stu-id="7521c-111">Begin</span></span></td>
<td><span data-ttu-id="7521c-112">Обратный вызов для начала операции.</span><span class="sxs-lookup"><span data-stu-id="7521c-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7521c-113">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="7521c-113">Progress</span></span></td>
<td><span data-ttu-id="7521c-114">Обратный вызов для хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7521c-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7521c-115">Завершить</span><span class="sxs-lookup"><span data-stu-id="7521c-115">Complete</span></span></td>
<td><span data-ttu-id="7521c-116">Обратный вызов для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7521c-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7521c-117">Ошибка</span><span class="sxs-lookup"><span data-stu-id="7521c-117">Fail</span></span></td>
<td><span data-ttu-id="7521c-118">Обратный вызов для сбоя во время операции.</span><span class="sxs-lookup"><span data-stu-id="7521c-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7521c-119">рековеристеп</span><span class="sxs-lookup"><span data-stu-id="7521c-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="7521c-120">Обратный вызов для управления восстановлением.</span><span class="sxs-lookup"><span data-stu-id="7521c-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="7521c-121">Используется для внутренней обработки в версиях операционной системы Windows, предшествующих Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7521c-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="7521c-122">Это значение неприменимо к версиям Windows, начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7521c-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7521c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7521c-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7521c-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="7521c-124">Reference</span></span>

[<span data-ttu-id="7521c-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7521c-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о: Есентрекорднотделетедексцептион Class'
title: Класс Есентрекорднотделетедексцептион
TOCTitle: EsentRecordNotDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnotdeletedexception(v=EXCHG.10)
ms:contentKeyID: 55102578
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70eb38e960b127474415c9b7291e4765719fb7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711237"
---
# <a name="esentrecordnotdeletedexception-class"></a><span data-ttu-id="00fe1-103">Класс Есентрекорднотделетедексцептион</span><span class="sxs-lookup"><span data-stu-id="00fe1-103">EsentRecordNotDeletedException class</span></span>

<span data-ttu-id="00fe1-104">Базовый класс для JET_err. Исключения Рекорднотделетед.</span><span class="sxs-lookup"><span data-stu-id="00fe1-104">Base class for JET_err.RecordNotDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="00fe1-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="00fe1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="00fe1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="00fe1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="00fe1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="00fe1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="00fe1-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="00fe1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="00fe1-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="00fe1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="00fe1-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="00fe1-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="00fe1-111">Microsoft. ISAM. ESENT. Interop. Есентрекорднотделетедексцептион</span><span class="sxs-lookup"><span data-stu-id="00fe1-111">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>  

<span data-ttu-id="00fe1-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00fe1-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="00fe1-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="00fe1-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00fe1-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00fe1-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNotDeletedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentRecordNotDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNotDeletedException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="00fe1-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="00fe1-115">Thread safety</span></span>

<span data-ttu-id="00fe1-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="00fe1-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="00fe1-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="00fe1-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="00fe1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00fe1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00fe1-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="00fe1-119">Reference</span></span>

[<span data-ttu-id="00fe1-120">Элементы Есентрекорднотделетедексцептион</span><span class="sxs-lookup"><span data-stu-id="00fe1-120">EsentRecordNotDeletedException members</span></span>](./esentrecordnotdeletedexception-members.md)

[<span data-ttu-id="00fe1-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="00fe1-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

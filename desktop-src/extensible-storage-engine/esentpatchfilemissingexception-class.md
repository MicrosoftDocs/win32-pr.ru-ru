---
description: 'Дополнительные сведения о: Есентпатчфилемиссинжексцептион Class'
title: Класс Есентпатчфилемиссинжексцептион
TOCTitle: EsentPatchFileMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpatchfilemissingexception(v=EXCHG.10)
ms:contentKeyID: 55102469
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edaabc35018c7905542f9a7325efaed300234e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347592"
---
# <a name="esentpatchfilemissingexception-class"></a><span data-ttu-id="2e2b3-103">Класс Есентпатчфилемиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-103">EsentPatchFileMissingException class</span></span>

<span data-ttu-id="2e2b3-104">Базовый класс для JET_err. Исключения Патчфилемиссинг.</span><span class="sxs-lookup"><span data-stu-id="2e2b3-104">Base class for JET_err.PatchFileMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e2b3-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="2e2b3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e2b3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e2b3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2e2b3-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2e2b3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2e2b3-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2e2b3-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2e2b3-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2e2b3-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="2e2b3-112">Microsoft. ISAM. ESENT. Interop. Есентпатчфилемиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-112">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>  

<span data-ttu-id="2e2b3-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e2b3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e2b3-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e2b3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2b3-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e2b3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPatchFileMissingException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentPatchFileMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPatchFileMissingException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="2e2b3-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="2e2b3-116">Thread safety</span></span>

<span data-ttu-id="2e2b3-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="2e2b3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e2b3-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="2e2b3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e2b3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e2b3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e2b3-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="2e2b3-120">Reference</span></span>

[<span data-ttu-id="2e2b3-121">Элементы Есентпатчфилемиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="2e2b3-121">EsentPatchFileMissingException members</span></span>](./esentpatchfilemissingexception-members.md)

[<span data-ttu-id="2e2b3-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2e2b3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

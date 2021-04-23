---
description: 'Дополнительные сведения о: Есентсповнексткорруптедексцептион Class'
title: Класс Есентсповнексткорруптедексцептион
TOCTitle: EsentSPOwnExtCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspownextcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102983
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 15f3f37dfafcaa58d63a34c19d629f4469826cd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647569"
---
# <a name="esentspownextcorruptedexception-class"></a><span data-ttu-id="5dc73-103">Класс Есентсповнексткорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-103">EsentSPOwnExtCorruptedException class</span></span>

<span data-ttu-id="5dc73-104">Базовый класс для JET_err. Исключения Сповнексткорруптед.</span><span class="sxs-lookup"><span data-stu-id="5dc73-104">Base class for JET_err.SPOwnExtCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5dc73-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="5dc73-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5dc73-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5dc73-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5dc73-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5dc73-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5dc73-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5dc73-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5dc73-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="5dc73-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="5dc73-112">Microsoft. ISAM. ESENT. Interop. Есентсповнексткорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-112">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>  

<span data-ttu-id="5dc73-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5dc73-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5dc73-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5dc73-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc73-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dc73-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPOwnExtCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSPOwnExtCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPOwnExtCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="5dc73-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="5dc73-116">Thread safety</span></span>

<span data-ttu-id="5dc73-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="5dc73-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5dc73-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="5dc73-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dc73-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dc73-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5dc73-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="5dc73-120">Reference</span></span>

[<span data-ttu-id="5dc73-121">Элементы Есентсповнексткорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="5dc73-121">EsentSPOwnExtCorruptedException members</span></span>](./esentspownextcorruptedexception-members.md)

[<span data-ttu-id="5dc73-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5dc73-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о: Есентредоабруптендедексцептион Class'
title: Класс Есентредоабруптендедексцептион
TOCTitle: EsentRedoAbruptEndedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentredoabruptendedexception(v=EXCHG.10)
ms:contentKeyID: 55102536
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 436a03d5775c4d4bec405566c98280a3250e9196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702269"
---
# <a name="esentredoabruptendedexception-class"></a><span data-ttu-id="31400-103">Класс Есентредоабруптендедексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-103">EsentRedoAbruptEndedException class</span></span>

<span data-ttu-id="31400-104">Базовый класс для JET_err. Исключения Редоабруптендед.</span><span class="sxs-lookup"><span data-stu-id="31400-104">Base class for JET_err.RedoAbruptEnded exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="31400-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="31400-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="31400-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="31400-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="31400-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="31400-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="31400-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="31400-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="31400-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="31400-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="31400-112">Microsoft. ISAM. ESENT. Interop. Есентредоабруптендедексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-112">Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException</span></span>  

<span data-ttu-id="31400-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31400-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31400-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="31400-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31400-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31400-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRedoAbruptEndedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRedoAbruptEndedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRedoAbruptEndedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="31400-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="31400-116">Thread safety</span></span>

<span data-ttu-id="31400-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="31400-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="31400-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="31400-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="31400-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31400-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31400-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="31400-120">Reference</span></span>

[<span data-ttu-id="31400-121">Элементы Есентредоабруптендедексцептион</span><span class="sxs-lookup"><span data-stu-id="31400-121">EsentRedoAbruptEndedException members</span></span>](./esentredoabruptendedexception-members.md)

[<span data-ttu-id="31400-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="31400-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

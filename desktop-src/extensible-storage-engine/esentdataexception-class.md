---
description: 'Дополнительные сведения о: Есентдатаексцептион Class'
title: Класс Есентдатаексцептион
TOCTitle: EsentDataException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 996839740d1b008ffae12cf823b9664bf8ca4273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711597"
---
# <a name="esentdataexception-class"></a><span data-ttu-id="21b9e-103">Класс Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-103">EsentDataException class</span></span>

<span data-ttu-id="21b9e-104">Базовый класс для исключений данных.</span><span class="sxs-lookup"><span data-stu-id="21b9e-104">Base class for Data exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="21b9e-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="21b9e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="21b9e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="21b9e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="21b9e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="21b9e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="21b9e-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="21b9e-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="21b9e-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>  
          [<span data-ttu-id="21b9e-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
          [<span data-ttu-id="21b9e-112">Microsoft. ISAM. ESENT. Interop. Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-112">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
          [<span data-ttu-id="21b9e-113">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-113">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  

<span data-ttu-id="21b9e-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21b9e-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21b9e-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21b9e-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21b9e-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21b9e-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDataException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentDataException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDataException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="21b9e-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="21b9e-117">Thread safety</span></span>

<span data-ttu-id="21b9e-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="21b9e-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="21b9e-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="21b9e-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="21b9e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21b9e-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21b9e-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="21b9e-121">Reference</span></span>

[<span data-ttu-id="21b9e-122">Элементы Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="21b9e-122">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="21b9e-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="21b9e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

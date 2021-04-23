---
description: 'Дополнительные сведения о: Есентфилесистемкорруптионексцептион Class'
title: Класс Есентфилесистемкорруптионексцептион
TOCTitle: EsentFileSystemCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilesystemcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101716
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 863766b5b4b768546ade161abf8c30659db1d720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816665"
---
# <a name="esentfilesystemcorruptionexception-class"></a><span data-ttu-id="dd43d-103">Класс Есентфилесистемкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-103">EsentFileSystemCorruptionException class</span></span>

<span data-ttu-id="dd43d-104">Базовый класс для JET_err. Исключения Филесистемкорруптион.</span><span class="sxs-lookup"><span data-stu-id="dd43d-104">Base class for JET_err.FileSystemCorruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dd43d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="dd43d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dd43d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dd43d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dd43d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="dd43d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dd43d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dd43d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dd43d-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="dd43d-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="dd43d-112">Microsoft. ISAM. ESENT. Interop. Есентфилесистемкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-112">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>  

<span data-ttu-id="dd43d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd43d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd43d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd43d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd43d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd43d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileSystemCorruptionException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentFileSystemCorruptionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileSystemCorruptionException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="dd43d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="dd43d-116">Thread safety</span></span>

<span data-ttu-id="dd43d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="dd43d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dd43d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="dd43d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd43d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd43d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd43d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="dd43d-120">Reference</span></span>

[<span data-ttu-id="dd43d-121">Элементы Есентфилесистемкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="dd43d-121">EsentFileSystemCorruptionException members</span></span>](./esentfilesystemcorruptionexception-members.md)

[<span data-ttu-id="dd43d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dd43d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

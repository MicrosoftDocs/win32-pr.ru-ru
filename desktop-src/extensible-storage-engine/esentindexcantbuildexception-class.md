---
description: 'Дополнительные сведения о: Есентиндекскантбуилдексцептион Class'
title: Класс Есентиндекскантбуилдексцептион
TOCTitle: EsentIndexCantBuildException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexcantbuildexception(v=EXCHG.10)
ms:contentKeyID: 55101747
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf5443e58d2d158bc2145cf8ff922d073c83f3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701675"
---
# <a name="esentindexcantbuildexception-class"></a><span data-ttu-id="2ff7e-103">Класс Есентиндекскантбуилдексцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-103">EsentIndexCantBuildException class</span></span>

<span data-ttu-id="2ff7e-104">Базовый класс для JET_err. Исключения Индекскантбуилд.</span><span class="sxs-lookup"><span data-stu-id="2ff7e-104">Base class for JET_err.IndexCantBuild exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2ff7e-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="2ff7e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2ff7e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2ff7e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2ff7e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2ff7e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2ff7e-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2ff7e-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2ff7e-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2ff7e-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="2ff7e-112">Microsoft. ISAM. ESENT. Interop. Есентиндекскантбуилдексцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-112">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>  

<span data-ttu-id="2ff7e-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ff7e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ff7e-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2ff7e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff7e-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ff7e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexCantBuildException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentIndexCantBuildException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexCantBuildException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="2ff7e-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="2ff7e-116">Thread safety</span></span>

<span data-ttu-id="2ff7e-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="2ff7e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2ff7e-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="2ff7e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ff7e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ff7e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ff7e-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="2ff7e-120">Reference</span></span>

[<span data-ttu-id="2ff7e-121">Элементы Есентиндекскантбуилдексцептион</span><span class="sxs-lookup"><span data-stu-id="2ff7e-121">EsentIndexCantBuildException members</span></span>](./esentindexcantbuildexception-members.md)

[<span data-ttu-id="2ff7e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2ff7e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

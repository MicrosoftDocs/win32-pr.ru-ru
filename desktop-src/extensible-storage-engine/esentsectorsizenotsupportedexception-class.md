---
description: 'Дополнительные сведения о: Есентсекторсизенотсуппортедексцептион Class'
title: Класс Есентсекторсизенотсуппортедексцептион
TOCTitle: EsentSectorSizeNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsectorsizenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320c46869308296b697298f1e957f0cea8ca915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546943"
---
# <a name="esentsectorsizenotsupportedexception-class"></a><span data-ttu-id="09e14-103">Класс Есентсекторсизенотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-103">EsentSectorSizeNotSupportedException class</span></span>

<span data-ttu-id="09e14-104">Базовый класс для JET_err. Исключения Секторсизенотсуппортед.</span><span class="sxs-lookup"><span data-stu-id="09e14-104">Base class for JET_err.SectorSizeNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="09e14-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="09e14-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="09e14-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="09e14-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="09e14-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="09e14-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="09e14-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="09e14-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="09e14-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="09e14-111">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="09e14-112">Microsoft. ISAM. ESENT. Interop. Есентсекторсизенотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-112">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>  

<span data-ttu-id="09e14-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09e14-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09e14-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09e14-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09e14-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09e14-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSectorSizeNotSupportedException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentSectorSizeNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSectorSizeNotSupportedException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="09e14-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="09e14-116">Thread safety</span></span>

<span data-ttu-id="09e14-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="09e14-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="09e14-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="09e14-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="09e14-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09e14-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09e14-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="09e14-120">Reference</span></span>

[<span data-ttu-id="09e14-121">Элементы Есентсекторсизенотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="09e14-121">EsentSectorSizeNotSupportedException members</span></span>](./esentsectorsizenotsupportedexception-members.md)

[<span data-ttu-id="09e14-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="09e14-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

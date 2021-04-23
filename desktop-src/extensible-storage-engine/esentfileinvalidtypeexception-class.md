---
description: 'Дополнительные сведения о: Есентфилеинвалидтипиксцептион Class'
title: Класс Есентфилеинвалидтипиксцептион
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349162"
---
# <a name="esentfileinvalidtypeexception-class"></a><span data-ttu-id="33217-103">Класс Есентфилеинвалидтипиксцептион</span><span class="sxs-lookup"><span data-stu-id="33217-103">EsentFileInvalidTypeException class</span></span>

<span data-ttu-id="33217-104">Базовый класс для JET_err. Исключения Филеинвалидтипе.</span><span class="sxs-lookup"><span data-stu-id="33217-104">Base class for JET_err.FileInvalidType exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="33217-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="33217-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="33217-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="33217-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="33217-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="33217-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="33217-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="33217-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="33217-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="33217-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="33217-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="33217-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="33217-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="33217-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="33217-112">Microsoft. ISAM. ESENT. Interop. Есентфилеинвалидтипиксцептион</span><span class="sxs-lookup"><span data-stu-id="33217-112">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>  

<span data-ttu-id="33217-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33217-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33217-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33217-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33217-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33217-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="33217-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="33217-116">Thread safety</span></span>

<span data-ttu-id="33217-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="33217-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="33217-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="33217-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="33217-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33217-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33217-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="33217-120">Reference</span></span>

[<span data-ttu-id="33217-121">Элементы Есентфилеинвалидтипиксцептион</span><span class="sxs-lookup"><span data-stu-id="33217-121">EsentFileInvalidTypeException members</span></span>](./esentfileinvalidtypeexception-members.md)

[<span data-ttu-id="33217-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="33217-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

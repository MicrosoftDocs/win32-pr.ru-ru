---
description: 'Дополнительные сведения о: EsentDatabase200FormatException Class'
title: Класс EsentDatabase200FormatException
TOCTitle: EsentDatabase200FormatException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabase200formatexception(v=EXCHG.10)
ms:contentKeyID: 55101390
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33ee3c1d0a95d2e7abededc4544712e3a4893b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647519"
---
# <a name="esentdatabase200formatexception-class"></a><span data-ttu-id="47afc-103">Класс EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="47afc-103">EsentDatabase200FormatException class</span></span>

<span data-ttu-id="47afc-104">Базовый класс для JET_err. Исключения Database200Format.</span><span class="sxs-lookup"><span data-stu-id="47afc-104">Base class for JET_err.Database200Format exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="47afc-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="47afc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="47afc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="47afc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="47afc-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="47afc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="47afc-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="47afc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="47afc-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="47afc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="47afc-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="47afc-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="47afc-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="47afc-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="47afc-112">Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="47afc-112">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>  

<span data-ttu-id="47afc-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="47afc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="47afc-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="47afc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="47afc-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47afc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabase200FormatException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabase200FormatException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabase200FormatException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="47afc-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="47afc-116">Thread safety</span></span>

<span data-ttu-id="47afc-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="47afc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="47afc-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="47afc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="47afc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47afc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="47afc-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="47afc-120">Reference</span></span>

[<span data-ttu-id="47afc-121">Элементы EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="47afc-121">EsentDatabase200FormatException members</span></span>](./esentdatabase200formatexception-members.md)

[<span data-ttu-id="47afc-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="47afc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

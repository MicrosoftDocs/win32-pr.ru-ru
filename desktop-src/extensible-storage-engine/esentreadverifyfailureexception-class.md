---
description: 'Дополнительные сведения о: Есентреадверифифаилуриксцептион Class'
title: Класс Есентреадверифифаилуриксцептион
TOCTitle: EsentReadVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102552
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7a66cd94fc956947e08a919287aec7f04b07ea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701905"
---
# <a name="esentreadverifyfailureexception-class"></a><span data-ttu-id="d9620-103">Класс Есентреадверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-103">EsentReadVerifyFailureException class</span></span>

<span data-ttu-id="d9620-104">Базовый класс для JET_err. Исключения Реадверифифаилуре.</span><span class="sxs-lookup"><span data-stu-id="d9620-104">Base class for JET_err.ReadVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d9620-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="d9620-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d9620-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d9620-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d9620-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d9620-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d9620-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d9620-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d9620-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d9620-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="d9620-112">Microsoft. ISAM. ESENT. Interop. Есентреадверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-112">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>  

<span data-ttu-id="d9620-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9620-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9620-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9620-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9620-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9620-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="d9620-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="d9620-116">Thread safety</span></span>

<span data-ttu-id="d9620-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="d9620-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d9620-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="d9620-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9620-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9620-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9620-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="d9620-120">Reference</span></span>

[<span data-ttu-id="d9620-121">Элементы Есентреадверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="d9620-121">EsentReadVerifyFailureException members</span></span>](./esentreadverifyfailureexception-members.md)

[<span data-ttu-id="d9620-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d9620-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

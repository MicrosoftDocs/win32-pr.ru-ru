---
description: 'Дополнительные сведения о: Есентинвалиднамиксцептион Class'
title: Класс Есентинвалиднамиксцептион
TOCTitle: EsentInvalidNameException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidNameException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidnameexception(v=EXCHG.10)
ms:contentKeyID: 55101977
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidNameException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidNameException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0bc20287d26800478a5a41ff39b3bce08fb5eae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081047"
---
# <a name="esentinvalidnameexception-class"></a><span data-ttu-id="a1242-103">Класс Есентинвалиднамиксцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-103">EsentInvalidNameException class</span></span>

<span data-ttu-id="a1242-104">Базовый класс для JET_err. Исключения Инвалиднаме.</span><span class="sxs-lookup"><span data-stu-id="a1242-104">Base class for JET_err.InvalidName exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a1242-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="a1242-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a1242-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a1242-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a1242-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a1242-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a1242-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a1242-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a1242-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a1242-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a1242-112">Microsoft. ISAM. ESENT. Interop. Есентинвалиднамиксцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-112">Microsoft.Isam.Esent.Interop.EsentInvalidNameException</span></span>  

<span data-ttu-id="a1242-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a1242-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a1242-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a1242-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a1242-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1242-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidNameException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidNameException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidNameException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a1242-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a1242-116">Thread safety</span></span>

<span data-ttu-id="a1242-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a1242-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a1242-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a1242-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1242-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1242-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a1242-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="a1242-120">Reference</span></span>

[<span data-ttu-id="a1242-121">Элементы Есентинвалиднамиксцептион</span><span class="sxs-lookup"><span data-stu-id="a1242-121">EsentInvalidNameException members</span></span>](./esentinvalidnameexception-members.md)

[<span data-ttu-id="a1242-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a1242-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

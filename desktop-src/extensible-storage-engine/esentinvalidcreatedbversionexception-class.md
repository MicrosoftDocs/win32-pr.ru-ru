---
description: 'Дополнительные сведения о: Есентинвалидкреатедбверсионексцептион Class'
title: Класс Есентинвалидкреатедбверсионексцептион
TOCTitle: EsentInvalidCreateDbVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcreatedbversionexception(v=EXCHG.10)
ms:contentKeyID: 55101905
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 273b00900fece4afbb1329e25a36e50074e031dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898485"
---
# <a name="esentinvalidcreatedbversionexception-class"></a><span data-ttu-id="73cc7-103">Класс Есентинвалидкреатедбверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-103">EsentInvalidCreateDbVersionException class</span></span>

<span data-ttu-id="73cc7-104">Базовый класс для JET_err. Исключения Инвалидкреатедбверсион.</span><span class="sxs-lookup"><span data-stu-id="73cc7-104">Base class for JET_err.InvalidCreateDbVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="73cc7-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="73cc7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="73cc7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="73cc7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="73cc7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="73cc7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="73cc7-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="73cc7-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="73cc7-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="73cc7-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="73cc7-112">Microsoft. ISAM. ESENT. Interop. Есентинвалидкреатедбверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-112">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>  

<span data-ttu-id="73cc7-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="73cc7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="73cc7-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="73cc7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="73cc7-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73cc7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidCreateDbVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidCreateDbVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidCreateDbVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="73cc7-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="73cc7-116">Thread safety</span></span>

<span data-ttu-id="73cc7-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="73cc7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="73cc7-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="73cc7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="73cc7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73cc7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="73cc7-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="73cc7-120">Reference</span></span>

[<span data-ttu-id="73cc7-121">Элементы Есентинвалидкреатедбверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="73cc7-121">EsentInvalidCreateDbVersionException members</span></span>](./esentinvalidcreatedbversionexception-members.md)

[<span data-ttu-id="73cc7-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="73cc7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

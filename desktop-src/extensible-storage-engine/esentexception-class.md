---
description: 'Дополнительные сведения о: Есентексцептион Class'
title: Класс Есентексцептион (Microsoft. ISAM. ESENT)
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 775d63c6b1d234696790b1187538a6d1ee734a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703154"
---
# <a name="esentexception-class"></a><span data-ttu-id="72beb-103">Класс Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="72beb-103">EsentException class</span></span>

<span data-ttu-id="72beb-104">Базовый класс для исключений ESENT.</span><span class="sxs-lookup"><span data-stu-id="72beb-104">Base class for ESENT exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="72beb-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="72beb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="72beb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="72beb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="72beb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="72beb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    <span data-ttu-id="72beb-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="72beb-108">Microsoft.Isam.Esent.EsentException</span></span>  
      [<span data-ttu-id="72beb-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="72beb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
      [<span data-ttu-id="72beb-110">Microsoft. ISAM. ESENT. Interop. Есентинвалидколумнексцептион</span><span class="sxs-lookup"><span data-stu-id="72beb-110">Microsoft.Isam.Esent.Interop.EsentInvalidColumnException</span></span>](./esentinvalidcolumnexception-class.md)  

<span data-ttu-id="72beb-111">**Пространство имен:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="72beb-111">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="72beb-112">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="72beb-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="72beb-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72beb-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a><span data-ttu-id="72beb-114">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="72beb-114">Thread safety</span></span>

<span data-ttu-id="72beb-115">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="72beb-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="72beb-116">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="72beb-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="72beb-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72beb-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="72beb-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="72beb-118">Reference</span></span>

[<span data-ttu-id="72beb-119">Элементы Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="72beb-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="72beb-120">Пространство имен Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="72beb-120">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)

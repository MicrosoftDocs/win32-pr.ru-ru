---
description: 'Дополнительные сведения о: Есентупдатемустверсионексцептион Class'
title: Класс Есентупдатемустверсионексцептион
TOCTitle: EsentUpdateMustVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUpdateMustVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentupdatemustversionexception(v=EXCHG.10)
ms:contentKeyID: 55107338
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUpdateMustVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUpdateMustVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fad36eb0cddf7d54bbdd72786d0c43435ddc164d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693318"
---
# <a name="esentupdatemustversionexception-class"></a><span data-ttu-id="01858-103">Класс Есентупдатемустверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-103">EsentUpdateMustVersionException class</span></span>

<span data-ttu-id="01858-104">Базовый класс для JET_err. Исключения Упдатемустверсион.</span><span class="sxs-lookup"><span data-stu-id="01858-104">Base class for JET_err.UpdateMustVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="01858-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="01858-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="01858-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="01858-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="01858-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="01858-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="01858-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="01858-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="01858-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="01858-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="01858-112">Microsoft. ISAM. ESENT. Interop. Есентупдатемустверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-112">Microsoft.Isam.Esent.Interop.EsentUpdateMustVersionException</span></span>  

<span data-ttu-id="01858-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01858-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01858-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01858-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01858-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01858-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUpdateMustVersionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentUpdateMustVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUpdateMustVersionException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="01858-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="01858-116">Thread safety</span></span>

<span data-ttu-id="01858-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="01858-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="01858-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="01858-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="01858-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01858-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01858-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="01858-120">Reference</span></span>

[<span data-ttu-id="01858-121">Элементы Есентупдатемустверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="01858-121">EsentUpdateMustVersionException members</span></span>](./esentupdatemustversionexception-members.md)

[<span data-ttu-id="01858-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="01858-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

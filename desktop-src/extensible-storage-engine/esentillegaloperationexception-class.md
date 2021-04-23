---
description: 'Дополнительные сведения о: Есентиллегалоператионексцептион Class'
title: Класс Есентиллегалоператионексцептион
TOCTitle: EsentIllegalOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIllegalOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentillegaloperationexception(v=EXCHG.10)
ms:contentKeyID: 55101785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIllegalOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIllegalOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49767b6fa24edd713bbe320abcf82f606d47fd35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719676"
---
# <a name="esentillegaloperationexception-class"></a><span data-ttu-id="3e3c7-103">Класс Есентиллегалоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-103">EsentIllegalOperationException class</span></span>

<span data-ttu-id="3e3c7-104">Базовый класс для JET_err. Исключения Иллегалоператион.</span><span class="sxs-lookup"><span data-stu-id="3e3c7-104">Base class for JET_err.IllegalOperation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3e3c7-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="3e3c7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3e3c7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3e3c7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3e3c7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3e3c7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3e3c7-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3e3c7-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3e3c7-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3e3c7-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="3e3c7-112">Microsoft. ISAM. ESENT. Interop. Есентиллегалоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-112">Microsoft.Isam.Esent.Interop.EsentIllegalOperationException</span></span>  

<span data-ttu-id="3e3c7-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e3c7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3e3c7-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3e3c7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3c7-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e3c7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIllegalOperationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIllegalOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIllegalOperationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="3e3c7-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="3e3c7-116">Thread safety</span></span>

<span data-ttu-id="3e3c7-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="3e3c7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3e3c7-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3e3c7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e3c7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e3c7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e3c7-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="3e3c7-120">Reference</span></span>

[<span data-ttu-id="3e3c7-121">Элементы Есентиллегалоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="3e3c7-121">EsentIllegalOperationException members</span></span>](./esentillegaloperationexception-members.md)

[<span data-ttu-id="3e3c7-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3e3c7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

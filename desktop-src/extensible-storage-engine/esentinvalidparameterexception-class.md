---
description: 'Дополнительные сведения о: Есентинвалидпараметерексцептион Class'
title: Класс Есентинвалидпараметерексцептион
TOCTitle: EsentInvalidParameterException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidParameterException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidparameterexception(v=EXCHG.10)
ms:contentKeyID: 55102037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidParameterException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidParameterException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf94a4556762c68a886e5fab4b8f3fec2eeb003f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702825"
---
# <a name="esentinvalidparameterexception-class"></a><span data-ttu-id="0e31f-103">Класс Есентинвалидпараметерексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-103">EsentInvalidParameterException class</span></span>

<span data-ttu-id="0e31f-104">Базовый класс для JET_err. Исключения Инвалидпараметер.</span><span class="sxs-lookup"><span data-stu-id="0e31f-104">Base class for JET_err.InvalidParameter exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0e31f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="0e31f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0e31f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0e31f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0e31f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0e31f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0e31f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0e31f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0e31f-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0e31f-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0e31f-112">Microsoft. ISAM. ESENT. Interop. Есентинвалидпараметерексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-112">Microsoft.Isam.Esent.Interop.EsentInvalidParameterException</span></span>  

<span data-ttu-id="0e31f-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e31f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e31f-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e31f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e31f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e31f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidParameterException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidParameterException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidParameterException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0e31f-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="0e31f-116">Thread safety</span></span>

<span data-ttu-id="0e31f-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="0e31f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0e31f-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="0e31f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e31f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e31f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e31f-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="0e31f-120">Reference</span></span>

[<span data-ttu-id="0e31f-121">Элементы Есентинвалидпараметерексцептион</span><span class="sxs-lookup"><span data-stu-id="0e31f-121">EsentInvalidParameterException members</span></span>](./esentinvalidparameterexception-members.md)

[<span data-ttu-id="0e31f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0e31f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о: Есентаутофаутоинкрементвалуесексцептион Class'
title: Класс Есентаутофаутоинкрементвалуесексцептион
TOCTitle: EsentOutOfAutoincrementValuesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofautoincrementvaluesexception(v=EXCHG.10)
ms:contentKeyID: 55102440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a37a25e508281083915cf549db5a1b65a4bdcadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711808"
---
# <a name="esentoutofautoincrementvaluesexception-class"></a><span data-ttu-id="27633-103">Класс Есентаутофаутоинкрементвалуесексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-103">EsentOutOfAutoincrementValuesException class</span></span>

<span data-ttu-id="27633-104">Базовый класс для JET_err. Исключения Аутофаутоинкрементвалуес.</span><span class="sxs-lookup"><span data-stu-id="27633-104">Base class for JET_err.OutOfAutoincrementValues exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="27633-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="27633-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="27633-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="27633-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="27633-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="27633-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="27633-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="27633-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="27633-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="27633-111">Microsoft. ISAM. ESENT. Interop. Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="27633-112">Microsoft. ISAM. ESENT. Interop. Есентаутофаутоинкрементвалуесексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-112">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>  

<span data-ttu-id="27633-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27633-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27633-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27633-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27633-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27633-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfAutoincrementValuesException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfAutoincrementValuesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfAutoincrementValuesException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="27633-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="27633-116">Thread safety</span></span>

<span data-ttu-id="27633-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="27633-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="27633-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="27633-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="27633-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27633-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27633-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="27633-120">Reference</span></span>

[<span data-ttu-id="27633-121">Элементы Есентаутофаутоинкрементвалуесексцептион</span><span class="sxs-lookup"><span data-stu-id="27633-121">EsentOutOfAutoincrementValuesException members</span></span>](./esentoutofautoincrementvaluesexception-members.md)

[<span data-ttu-id="27633-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="27633-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

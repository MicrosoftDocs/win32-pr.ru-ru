---
description: 'Дополнительные сведения о: Есентроллбаккеррорексцептион Class'
title: Класс Есентроллбаккеррорексцептион
TOCTitle: EsentRollbackErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackerrorexception(v=EXCHG.10)
ms:contentKeyID: 55102663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e56e3e829b8c44ff6325ed877606fb44471f6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711581"
---
# <a name="esentrollbackerrorexception-class"></a><span data-ttu-id="a4297-103">Класс Есентроллбаккеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-103">EsentRollbackErrorException class</span></span>

<span data-ttu-id="a4297-104">Базовый класс для JET_err. Исключения Роллбаккеррор.</span><span class="sxs-lookup"><span data-stu-id="a4297-104">Base class for JET_err.RollbackError exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a4297-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="a4297-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a4297-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a4297-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a4297-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a4297-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a4297-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a4297-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a4297-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="a4297-111">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="a4297-112">Microsoft. ISAM. ESENT. Interop. Есентроллбаккеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-112">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>  

<span data-ttu-id="a4297-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4297-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4297-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a4297-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4297-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4297-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackErrorException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentRollbackErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackErrorException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="a4297-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a4297-116">Thread safety</span></span>

<span data-ttu-id="a4297-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a4297-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a4297-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a4297-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4297-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4297-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4297-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="a4297-120">Reference</span></span>

[<span data-ttu-id="a4297-121">Элементы Есентроллбаккеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a4297-121">EsentRollbackErrorException members</span></span>](./esentrollbackerrorexception-members.md)

[<span data-ttu-id="a4297-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a4297-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

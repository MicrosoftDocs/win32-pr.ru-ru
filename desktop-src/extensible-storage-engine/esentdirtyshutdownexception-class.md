---
description: 'Дополнительные сведения о: Есентдиртишутдовнексцептион Class'
title: Класс Есентдиртишутдовнексцептион
TOCTitle: EsentDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101504
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72eb3984c034cbbb9c6163e183a5b8680fc49845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712998"
---
# <a name="esentdirtyshutdownexception-class"></a><span data-ttu-id="4b949-103">Класс Есентдиртишутдовнексцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-103">EsentDirtyShutdownException class</span></span>

<span data-ttu-id="4b949-104">Базовый класс для JET_err. Исключения Диртишутдовн.</span><span class="sxs-lookup"><span data-stu-id="4b949-104">Base class for JET_err.DirtyShutdown exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4b949-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4b949-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4b949-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4b949-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4b949-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4b949-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4b949-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4b949-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4b949-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4b949-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="4b949-112">Microsoft. ISAM. ESENT. Interop. Есентдиртишутдовнексцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-112">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>  

<span data-ttu-id="4b949-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b949-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b949-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4b949-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b949-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b949-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDirtyShutdownException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDirtyShutdownException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="4b949-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4b949-116">Thread safety</span></span>

<span data-ttu-id="4b949-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4b949-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4b949-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4b949-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b949-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b949-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b949-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4b949-120">Reference</span></span>

[<span data-ttu-id="4b949-121">Элементы Есентдиртишутдовнексцептион</span><span class="sxs-lookup"><span data-stu-id="4b949-121">EsentDirtyShutdownException members</span></span>](./esentdirtyshutdownexception-members.md)

[<span data-ttu-id="4b949-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4b949-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

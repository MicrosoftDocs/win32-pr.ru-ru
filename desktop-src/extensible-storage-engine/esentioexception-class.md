---
description: 'Дополнительные сведения о: Есентиоексцептион Class'
title: Класс EsentIOException
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fbcbf38ae60ae17f74e650c403611a88d89662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703371"
---
# <a name="esentioexception-class"></a><span data-ttu-id="573c1-103">Класс EsentIOException</span><span class="sxs-lookup"><span data-stu-id="573c1-103">EsentIOException class</span></span>

<span data-ttu-id="573c1-104">Базовый класс для исключений операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="573c1-104">Base class for IO exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="573c1-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="573c1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="573c1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="573c1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="573c1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="573c1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="573c1-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="573c1-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="573c1-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="573c1-111">Microsoft. ISAM. ESENT. Interop. Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>  
            [<span data-ttu-id="573c1-112">Microsoft. ISAM. ESENT. Interop. Есентделетебаккупфилефаилексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-112">Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException</span></span>](./esentdeletebackupfilefailexception-class.md)  
            [<span data-ttu-id="573c1-113">Microsoft. ISAM. ESENT. Interop. Есентдискиоексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-113">Microsoft.Isam.Esent.Interop.EsentDiskIOException</span></span>](./esentdiskioexception-class.md)  
            [<span data-ttu-id="573c1-114">Microsoft. ISAM. ESENT. Interop. Есентфилеакцессдениедексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-114">Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException</span></span>](./esentfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="573c1-115">Microsoft. ISAM. ESENT. Interop. Есентлогвритефаилексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-115">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>](./esentlogwritefailexception-class.md)  
            [<span data-ttu-id="573c1-116">Microsoft. ISAM. ESENT. Interop. Есентмакебаккупдиректорифаилексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-116">Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException</span></span>](./esentmakebackupdirectoryfailexception-class.md)  

<span data-ttu-id="573c1-117">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="573c1-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="573c1-118">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="573c1-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="573c1-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="573c1-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="573c1-120">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="573c1-120">Thread safety</span></span>

<span data-ttu-id="573c1-121">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="573c1-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="573c1-122">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="573c1-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="573c1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="573c1-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="573c1-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="573c1-124">Reference</span></span>

[<span data-ttu-id="573c1-125">Элементы Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="573c1-125">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="573c1-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="573c1-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

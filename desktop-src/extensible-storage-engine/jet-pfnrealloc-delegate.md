---
description: 'Дополнительные сведения о: JET_PFNREALLOC делегата'
title: JET_PFNREALLOC делегат
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999625"
---
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="e25e8-103">JET_PFNREALLOC делегат</span><span class="sxs-lookup"><span data-stu-id="e25e8-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="e25e8-104">Обратный вызов, используемый Жетенумератеколумнс для выделения памяти для буферов вывода.</span><span class="sxs-lookup"><span data-stu-id="e25e8-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="e25e8-105">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="e25e8-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="e25e8-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e25e8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e25e8-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e25e8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e25e8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e25e8-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a><span data-ttu-id="e25e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e25e8-109">Parameters</span></span>

  - <span data-ttu-id="e25e8-110">контекст</span><span class="sxs-lookup"><span data-stu-id="e25e8-110">context</span></span>  
    <span data-ttu-id="e25e8-111">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e25e8-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="e25e8-112">Контекст, заданный для Жетенумератеколумнс.</span><span class="sxs-lookup"><span data-stu-id="e25e8-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="e25e8-113">Память</span><span class="sxs-lookup"><span data-stu-id="e25e8-113">memory</span></span>  
    <span data-ttu-id="e25e8-114">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e25e8-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="e25e8-115">Если ненулевое значение, указатель на блок памяти, ранее выделенный этим обратным вызовом.</span><span class="sxs-lookup"><span data-stu-id="e25e8-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="e25e8-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="e25e8-116">requestedSize</span></span>  
    <span data-ttu-id="e25e8-117">Тип: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="e25e8-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="e25e8-118">Новый размер блока памяти (в байтах).</span><span class="sxs-lookup"><span data-stu-id="e25e8-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="e25e8-119">Если это значение равно 0 и указан блок памяти, то этот блок памяти будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="e25e8-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e25e8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e25e8-120">Return value</span></span>

<span data-ttu-id="e25e8-121">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e25e8-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="e25e8-122">Указатель на только что выделенную память.</span><span class="sxs-lookup"><span data-stu-id="e25e8-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="e25e8-123">Если память не может быть выделена, возвращается [нуль](/dotnet/api/system.intptr.zero) .</span><span class="sxs-lookup"><span data-stu-id="e25e8-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e25e8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e25e8-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e25e8-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="e25e8-125">Reference</span></span>

[<span data-ttu-id="e25e8-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e25e8-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

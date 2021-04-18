---
description: 'Дополнительные сведения о: JET_PFNSTATUS делегата'
title: JET_PFNSTATUS делегат
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693361"
---
# <a name="jet_pfnstatus-delegate"></a><span data-ttu-id="fac5c-103">JET_PFNSTATUS делегат</span><span class="sxs-lookup"><span data-stu-id="fac5c-103">JET_PFNSTATUS delegate</span></span>

<span data-ttu-id="fac5c-104">Получает сведения о ходе выполнения длительных операций, таких как дефрагментация, операции резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="fac5c-104">Receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="fac5c-105">Во время таких операций ядро СУБД вызывает эту функцию обратного вызова, чтобы обеспечить обновление хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="fac5c-105">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

<span data-ttu-id="fac5c-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fac5c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fac5c-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fac5c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fac5c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fac5c-108">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a><span data-ttu-id="fac5c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fac5c-109">Parameters</span></span>

  - <span data-ttu-id="fac5c-110">сесид</span><span class="sxs-lookup"><span data-stu-id="fac5c-110">sesid</span></span>  
    <span data-ttu-id="fac5c-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fac5c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fac5c-112">Сеанс, с которым была вызвана долго выполняющаяся операция.</span><span class="sxs-lookup"><span data-stu-id="fac5c-112">The session with which the long running operation was called.</span></span>

<!-- end list -->

  - <span data-ttu-id="fac5c-113">Network</span><span class="sxs-lookup"><span data-stu-id="fac5c-113">snp</span></span>  
    <span data-ttu-id="fac5c-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SNP](./jet-snp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fac5c-114">Type: [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span></span>  
    
    <span data-ttu-id="fac5c-115">Тип операции.</span><span class="sxs-lookup"><span data-stu-id="fac5c-115">The type of operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="fac5c-116">снт</span><span class="sxs-lookup"><span data-stu-id="fac5c-116">snt</span></span>  
    <span data-ttu-id="fac5c-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SNT](./jet-snt-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fac5c-117">Type: [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span></span>  
    
    <span data-ttu-id="fac5c-118">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="fac5c-118">The status of the operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="fac5c-119">.</span><span class="sxs-lookup"><span data-stu-id="fac5c-119">data</span></span>  
    <span data-ttu-id="fac5c-120">Тип: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="fac5c-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="fac5c-121">Необязательные данные.</span><span class="sxs-lookup"><span data-stu-id="fac5c-121">Optional data.</span></span> <span data-ttu-id="fac5c-122">Может быть [JET_SNPROG](./jet-snprog-class.md).</span><span class="sxs-lookup"><span data-stu-id="fac5c-122">May be a [JET_SNPROG](./jet-snprog-class.md).</span></span>

#### <a name="return-value"></a><span data-ttu-id="fac5c-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fac5c-123">Return value</span></span>

<span data-ttu-id="fac5c-124">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fac5c-124">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fac5c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac5c-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fac5c-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="fac5c-126">Reference</span></span>

[<span data-ttu-id="fac5c-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fac5c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

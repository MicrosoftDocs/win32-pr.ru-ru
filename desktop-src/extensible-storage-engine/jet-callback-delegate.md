---
description: 'Дополнительные сведения о: JET_CALLBACK делегата'
title: JET_CALLBACK делегат
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674232"
---
# <a name="jet_callback-delegate"></a><span data-ttu-id="9621f-103">JET_CALLBACK делегат</span><span class="sxs-lookup"><span data-stu-id="9621f-103">JET_CALLBACK delegate</span></span>

<span data-ttu-id="9621f-104">Функция обратного вызова с множественной назначением, используемая ядром СУБД для информирования приложения о событии, включающем в себя оперативную дефрагментацию и уведомления о состоянии курсоров.</span><span class="sxs-lookup"><span data-stu-id="9621f-104">A multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="9621f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9621f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9621f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9621f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9621f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9621f-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a><span data-ttu-id="9621f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9621f-108">Parameters</span></span>

  - <span data-ttu-id="9621f-109">сесид</span><span class="sxs-lookup"><span data-stu-id="9621f-109">sesid</span></span>  
    <span data-ttu-id="9621f-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9621f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9621f-111">Сеанс, для которого выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="9621f-111">The session for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9621f-112">dbid</span></span>  
    <span data-ttu-id="9621f-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9621f-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9621f-114">База данных, для которой выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="9621f-114">The database for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-115">TableID</span><span class="sxs-lookup"><span data-stu-id="9621f-115">tableid</span></span>  
    <span data-ttu-id="9621f-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9621f-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9621f-117">Курсор, для которого выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="9621f-117">The cursor for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-118">кбтип</span><span class="sxs-lookup"><span data-stu-id="9621f-118">cbtyp</span></span>  
    <span data-ttu-id="9621f-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9621f-119">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="9621f-120">Операция, для которой выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="9621f-120">The operation for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-121">arg1</span><span class="sxs-lookup"><span data-stu-id="9621f-121">arg1</span></span>  
    <span data-ttu-id="9621f-122">Тип: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="9621f-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="9621f-123">Первый аргумент, зависящий от обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9621f-123">First callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-124">arg2</span><span class="sxs-lookup"><span data-stu-id="9621f-124">arg2</span></span>  
    <span data-ttu-id="9621f-125">Тип: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="9621f-125">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="9621f-126">Второй аргумент, зависящий от ответного вызова.</span><span class="sxs-lookup"><span data-stu-id="9621f-126">Second callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-127">контекст</span><span class="sxs-lookup"><span data-stu-id="9621f-127">context</span></span>  
    <span data-ttu-id="9621f-128">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="9621f-128">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="9621f-129">Контекст обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9621f-129">Callback context.</span></span>

<!-- end list -->

  - <span data-ttu-id="9621f-130">unused</span><span class="sxs-lookup"><span data-stu-id="9621f-130">unused</span></span>  
    <span data-ttu-id="9621f-131">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="9621f-131">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="9621f-132">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="9621f-132">This parameter is not used.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9621f-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9621f-133">Return value</span></span>

<span data-ttu-id="9621f-134">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9621f-134">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9621f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9621f-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9621f-136">Справочник</span><span class="sxs-lookup"><span data-stu-id="9621f-136">Reference</span></span>

[<span data-ttu-id="9621f-137">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9621f-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

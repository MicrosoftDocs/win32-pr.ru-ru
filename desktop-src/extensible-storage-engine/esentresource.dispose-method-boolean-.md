---
description: 'Дополнительные сведения о методе: Есентресаурце. Dispose (Boolean)'
title: Есентресаурце. Dispose-метод (Boolean)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf74291bf4c54ffa1d61c28bf7caff1e8c2b231b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272891"
---
# <a name="esentresourcedispose-method-boolean"></a><span data-ttu-id="730e3-103">Есентресаурце. Dispose-метод (Boolean)</span><span class="sxs-lookup"><span data-stu-id="730e3-103">EsentResource.Dispose method (Boolean)</span></span>

<span data-ttu-id="730e3-104">Вызывается методом Dispose и методом завершения.</span><span class="sxs-lookup"><span data-stu-id="730e3-104">Called by Dispose and the finalizer.</span></span>

<span data-ttu-id="730e3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="730e3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="730e3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="730e3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="730e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="730e3-107">Syntax</span></span>

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a><span data-ttu-id="730e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="730e3-108">Parameters</span></span>

  - <span data-ttu-id="730e3-109">Удаление</span><span class="sxs-lookup"><span data-stu-id="730e3-109">isDisposing</span></span>  
    <span data-ttu-id="730e3-110">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="730e3-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
    
    <span data-ttu-id="730e3-111">Значение true, если вызывается из Dispose.</span><span class="sxs-lookup"><span data-stu-id="730e3-111">True if called from Dispose.</span></span>

## <a name="see-also"></a><span data-ttu-id="730e3-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="730e3-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="730e3-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="730e3-113">Reference</span></span>

[<span data-ttu-id="730e3-114">Класс Есентресаурце</span><span class="sxs-lookup"><span data-stu-id="730e3-114">EsentResource class</span></span>](./esentresource-class.md)

[<span data-ttu-id="730e3-115">Элементы Есентресаурце</span><span class="sxs-lookup"><span data-stu-id="730e3-115">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="730e3-116">Перегрузка Dispose</span><span class="sxs-lookup"><span data-stu-id="730e3-116">Dispose overload</span></span>](./esentresource.dispose-method.md)

[<span data-ttu-id="730e3-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="730e3-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

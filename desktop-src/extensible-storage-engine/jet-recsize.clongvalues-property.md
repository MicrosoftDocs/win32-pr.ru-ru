---
description: 'Дополнительные сведения о свойстве: JET_RECSIZE. Клонгвалуес'
title: Свойство JET_RECSIZE. Клонгвалуес (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cLongValues property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.clongvalues(v=EXCHG.10)
ms:contentKeyID: 39515366
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cLongValues
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cLongValues
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cLongValues
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ba70428ccc6ceb1d03fe5109d6bf5c0d17e7831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710884"
---
# <a name="jet_recsizeclongvalues-property"></a><span data-ttu-id="d8f18-103">Свойство JET_RECSIZE. Клонгвалуес</span><span class="sxs-lookup"><span data-stu-id="d8f18-103">JET_RECSIZE.cLongValues property</span></span>

<span data-ttu-id="d8f18-104">Возвращает общее количество значений long, хранящихся в дереве Long-Value для этой записи.</span><span class="sxs-lookup"><span data-stu-id="d8f18-104">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="d8f18-105">Это не относится к внутренним длинным значениям.</span><span class="sxs-lookup"><span data-stu-id="d8f18-105">This does not include intrinsic long values.</span></span>

<span data-ttu-id="d8f18-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d8f18-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d8f18-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d8f18-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f18-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8f18-108">Syntax</span></span>

``` vb
'Declaration
Public Property cLongValues As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cLongValues
```

``` csharp
public long cLongValues { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="d8f18-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d8f18-109">Property value</span></span>

<span data-ttu-id="d8f18-110">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="d8f18-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8f18-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8f18-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d8f18-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="d8f18-112">Reference</span></span>

[<span data-ttu-id="d8f18-113">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="d8f18-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="d8f18-114">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="d8f18-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="d8f18-115">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="d8f18-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

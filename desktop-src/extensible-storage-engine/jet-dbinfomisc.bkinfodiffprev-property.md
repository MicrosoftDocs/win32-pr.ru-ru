---
description: 'Дополнительные сведения о свойстве: JET_DBINFOMISC. Бкинфодиффпрев'
title: Свойство JET_DBINFOMISC. Бкинфодиффпрев
TOCTitle: 'bkinfoDiffPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfodiffprev(v=EXCHG.10)
ms:contentKeyID: 39513441
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoDiffPrev
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd152d1dffbc4cf956129dfd886186dda0b33084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701487"
---
# <a name="jet_dbinfomiscbkinfodiffprev-property"></a><span data-ttu-id="14a52-103">Свойство JET_DBINFOMISC. Бкинфодиффпрев</span><span class="sxs-lookup"><span data-stu-id="14a52-103">JET_DBINFOMISC.bkinfoDiffPrev property</span></span>

<span data-ttu-id="14a52-104">Возвращает сведения о последней успешной разностной резервной копии.</span><span class="sxs-lookup"><span data-stu-id="14a52-104">Gets information about the last successful differential backup.</span></span> <span data-ttu-id="14a52-105">Сброс при установке [бкинфофуллпрев](./jet-dbinfomisc.bkinfofullprev-property.md) .</span><span class="sxs-lookup"><span data-stu-id="14a52-105">Reset when [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) is set.</span></span>

<span data-ttu-id="14a52-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14a52-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14a52-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14a52-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14a52-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14a52-108">Syntax</span></span>

``` vb
'Declaration
Public Property bkinfoDiffPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoDiffPrev
```

``` csharp
public JET_BKINFO bkinfoDiffPrev { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="14a52-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="14a52-109">Property value</span></span>

<span data-ttu-id="14a52-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="14a52-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="14a52-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14a52-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14a52-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="14a52-112">Reference</span></span>

[<span data-ttu-id="14a52-113">Класс JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="14a52-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="14a52-114">Элементы JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="14a52-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="14a52-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="14a52-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

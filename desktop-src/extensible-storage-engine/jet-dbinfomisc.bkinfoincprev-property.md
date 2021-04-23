---
description: 'Дополнительные сведения о свойстве: JET_DBINFOMISC. Бкинфоинкпрев'
title: Свойство JET_DBINFOMISC. Бкинфоинкпрев
TOCTitle: 'bkinfoIncPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfoincprev(v=EXCHG.10)
ms:contentKeyID: 39510848
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d323c9af95a59895b30c55cc0a2a5b2664a1c043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692136"
---
# <a name="jet_dbinfomiscbkinfoincprev-property"></a><span data-ttu-id="b25d6-103">Свойство JET_DBINFOMISC. Бкинфоинкпрев</span><span class="sxs-lookup"><span data-stu-id="b25d6-103">JET_DBINFOMISC.bkinfoIncPrev property</span></span>

<span data-ttu-id="b25d6-104">Возвращает сведения о последнем успешном добавочном резервном копировании.</span><span class="sxs-lookup"><span data-stu-id="b25d6-104">Gets information about the last successful incremental backup.</span></span> <span data-ttu-id="b25d6-105">Это значение сбрасывается при установке [бкинфофуллпрев](./jet-dbinfomisc.bkinfofullprev-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b25d6-105">This value is reset when [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) is set.</span></span>

<span data-ttu-id="b25d6-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b25d6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b25d6-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b25d6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b25d6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b25d6-108">Syntax</span></span>

``` vb
'Declaration
Public Property bkinfoIncPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoIncPrev
```

``` csharp
public JET_BKINFO bkinfoIncPrev { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="b25d6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b25d6-109">Property value</span></span>

<span data-ttu-id="b25d6-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b25d6-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b25d6-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b25d6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b25d6-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="b25d6-112">Reference</span></span>

[<span data-ttu-id="b25d6-113">Класс JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="b25d6-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="b25d6-114">Элементы JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="b25d6-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="b25d6-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b25d6-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

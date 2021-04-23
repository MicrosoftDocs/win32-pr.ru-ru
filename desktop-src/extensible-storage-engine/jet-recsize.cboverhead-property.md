---
description: 'Дополнительные сведения о свойстве: JET_RECSIZE. Кбоверхеад'
title: Свойство JET_RECSIZE. Кбоверхеад (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbOverhead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cboverhead(v=EXCHG.10)
ms:contentKeyID: 39514763
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbOverhead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e7318428ef4b50a08a05f5021d293ad1d8d78cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692134"
---
# <a name="jet_recsizecboverhead-property"></a><span data-ttu-id="de520-103">Свойство JET_RECSIZE. Кбоверхеад</span><span class="sxs-lookup"><span data-stu-id="de520-103">JET_RECSIZE.cbOverhead property</span></span>

<span data-ttu-id="de520-104">Возвращает дополнительную нагрузку на структуру записи ESENT для этой записи.</span><span class="sxs-lookup"><span data-stu-id="de520-104">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="de520-105">Сюда входит размер ключа записи.</span><span class="sxs-lookup"><span data-stu-id="de520-105">This includes the record's key size.</span></span>

<span data-ttu-id="de520-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="de520-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="de520-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="de520-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="de520-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de520-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbOverhead As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbOverhead
```

``` csharp
public long cbOverhead { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="de520-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="de520-109">Property value</span></span>

<span data-ttu-id="de520-110">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="de520-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="de520-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de520-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="de520-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="de520-112">Reference</span></span>

[<span data-ttu-id="de520-113">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="de520-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="de520-114">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="de520-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="de520-115">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="de520-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

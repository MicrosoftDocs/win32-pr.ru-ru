---
description: 'Дополнительные сведения о свойстве: Индексинфо. Индекссегментс'
title: Индексинфо. Индекссегментс, свойство
TOCTitle: 'IndexSegments property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.indexsegments(v=EXCHG.10)
ms:contentKeyID: 55103239
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
- Microsoft.Isam.Esent.Interop.IndexInfo.get_IndexSegments
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d366d3ddd5ba7a33faeb44459830dbaadcc221e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811164"
---
# <a name="indexinfoindexsegments-property"></a><span data-ttu-id="e0f25-103">Индексинфо. Индекссегментс, свойство</span><span class="sxs-lookup"><span data-stu-id="e0f25-103">IndexInfo.IndexSegments property</span></span>

<span data-ttu-id="e0f25-104">Возвращает сегменты индекса.</span><span class="sxs-lookup"><span data-stu-id="e0f25-104">Gets the segments of the index.</span></span>

<span data-ttu-id="e0f25-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0f25-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e0f25-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0f25-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f25-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0f25-107">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property IndexSegments As IList(Of IndexSegment)
    Get
'Usage
Dim instance As IndexInfo
Dim value As IList(Of IndexSegment)

value = instance.IndexSegments
```

``` csharp
public IList<IndexSegment> IndexSegments { get; }
```

#### <a name="property-value"></a><span data-ttu-id="e0f25-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e0f25-108">Property value</span></span>

<span data-ttu-id="e0f25-109">Тип: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[IndexSegment](./indexsegment-class.md)\></span><span class="sxs-lookup"><span data-stu-id="e0f25-109">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[IndexSegment](./indexsegment-class.md)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="e0f25-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0f25-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0f25-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="e0f25-111">Reference</span></span>

[<span data-ttu-id="e0f25-112">Класс Индексинфо</span><span class="sxs-lookup"><span data-stu-id="e0f25-112">IndexInfo class</span></span>](./indexinfo-class.md)

[<span data-ttu-id="e0f25-113">Элементы Индексинфо</span><span class="sxs-lookup"><span data-stu-id="e0f25-113">IndexInfo members</span></span>](./indexinfo-members.md)

[<span data-ttu-id="e0f25-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e0f25-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

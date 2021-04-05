---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидгрбитиндекс'
title: Свойство JET_INDEXLIST. Колумнидгрбитиндекс
TOCTitle: 'columnidgrbitIndex property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitindex(v=EXCHG.10)
ms:contentKeyID: 55103615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitIndex
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae8d31661451a2bd1c7c5f942141c27ae552c578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911763"
---
# <a name="jet_indexlistcolumnidgrbitindex-property"></a><span data-ttu-id="abf01-103">Свойство JET_INDEXLIST. Колумнидгрбитиндекс</span><span class="sxs-lookup"><span data-stu-id="abf01-103">JET_INDEXLIST.columnidgrbitIndex property</span></span>

<span data-ttu-id="abf01-104">Возвращает значение columnid столбца во временной таблице, в котором хранится грбитс, используемый в индексе.</span><span class="sxs-lookup"><span data-stu-id="abf01-104">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="abf01-105">См. [креатеиндексгрбит](./createindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="abf01-105">See [CreateIndexGrbit](./createindexgrbit-enumeration.md).</span></span> <span data-ttu-id="abf01-106">Столбец имеет тип [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="abf01-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="abf01-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="abf01-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="abf01-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="abf01-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="abf01-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abf01-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidgrbitIndex As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitIndex
```

``` csharp
public JET_COLUMNID columnidgrbitIndex { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="abf01-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="abf01-110">Property value</span></span>

<span data-ttu-id="abf01-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="abf01-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="abf01-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abf01-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="abf01-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="abf01-113">Reference</span></span>

[<span data-ttu-id="abf01-114">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="abf01-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="abf01-115">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="abf01-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="abf01-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="abf01-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

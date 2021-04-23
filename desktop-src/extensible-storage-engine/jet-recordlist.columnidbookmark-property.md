---
description: 'Дополнительные сведения о свойстве: JET_RECORDLIST. Колумнидбукмарк'
title: Свойство JET_RECORDLIST. Колумнидбукмарк
TOCTitle: 'columnidBookmark property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.columnidbookmark(v=EXCHG.10)
ms:contentKeyID: 55103827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2069a274c5d89b3198113985a11a5d8af26fd1a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272402"
---
# <a name="jet_recordlistcolumnidbookmark-property"></a><span data-ttu-id="bb1b0-103">Свойство JET_RECORDLIST. Колумнидбукмарк</span><span class="sxs-lookup"><span data-stu-id="bb1b0-103">JET_RECORDLIST.columnidBookmark property</span></span>

<span data-ttu-id="bb1b0-104">Возвращает значение columnid столбца во временной таблице, в котором хранится закладка записи.</span><span class="sxs-lookup"><span data-stu-id="bb1b0-104">Gets the columnid of the column in the temporary table which stores the bookmark of the record.</span></span> <span data-ttu-id="bb1b0-105">Столбец имеет тип JET_coltyp. Полнотекстовым.</span><span class="sxs-lookup"><span data-stu-id="bb1b0-105">The column is of type JET_coltyp.Text.</span></span>

<span data-ttu-id="bb1b0-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bb1b0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bb1b0-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bb1b0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1b0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb1b0-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidBookmark As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_COLUMNID

value = instance.columnidBookmark
```

``` csharp
public JET_COLUMNID columnidBookmark { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="bb1b0-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bb1b0-109">Property value</span></span>

<span data-ttu-id="bb1b0-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bb1b0-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb1b0-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb1b0-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb1b0-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="bb1b0-112">Reference</span></span>

[<span data-ttu-id="bb1b0-113">Класс JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="bb1b0-113">JET_RECORDLIST class</span></span>](./jet-recordlist-class.md)

[<span data-ttu-id="bb1b0-114">Элементы JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="bb1b0-114">JET_RECORDLIST members</span></span>](./jet-recordlist-members.md)

[<span data-ttu-id="bb1b0-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bb1b0-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

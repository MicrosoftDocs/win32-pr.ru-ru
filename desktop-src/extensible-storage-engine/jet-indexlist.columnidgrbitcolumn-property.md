---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидгрбитколумн'
title: Свойство JET_INDEXLIST. Колумнидгрбитколумн
TOCTitle: 'columnidgrbitColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitcolumn(v=EXCHG.10)
ms:contentKeyID: 55103665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18be8455f2618265d77991b7c839f21ff04ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712591"
---
# <a name="jet_indexlistcolumnidgrbitcolumn-property"></a><span data-ttu-id="f09f3-103">Свойство JET_INDEXLIST. Колумнидгрбитколумн</span><span class="sxs-lookup"><span data-stu-id="f09f3-103">JET_INDEXLIST.columnidgrbitColumn property</span></span>

<span data-ttu-id="f09f3-104">Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу.</span><span class="sxs-lookup"><span data-stu-id="f09f3-104">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="f09f3-105">См. [индекскэйгрбит](./indexkeygrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f09f3-105">See [IndexKeyGrbit](./indexkeygrbit-enumeration.md).</span></span> <span data-ttu-id="f09f3-106">Столбец имеет тип [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f09f3-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="f09f3-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f09f3-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f09f3-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f09f3-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f09f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f09f3-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidgrbitColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitColumn
```

``` csharp
public JET_COLUMNID columnidgrbitColumn { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="f09f3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f09f3-110">Property value</span></span>

<span data-ttu-id="f09f3-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f09f3-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f09f3-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f09f3-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f09f3-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="f09f3-113">Reference</span></span>

[<span data-ttu-id="f09f3-114">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="f09f3-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="f09f3-115">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="f09f3-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="f09f3-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f09f3-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

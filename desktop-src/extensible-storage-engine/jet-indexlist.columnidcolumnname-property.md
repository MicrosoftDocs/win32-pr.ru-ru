---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. колумнидколумннаме'
title: Свойство JET_INDEXLIST. колумнидколумннаме
TOCTitle: 'columnidcolumnname property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcolumnname(v=EXCHG.10)
ms:contentKeyID: 55103662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcolumnname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcolumnname
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcolumnname
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54968c88c854bd1fbc4760588e8bddeffdc88fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650832"
---
# <a name="jet_indexlistcolumnidcolumnname-property"></a><span data-ttu-id="80d44-103">Свойство JET_INDEXLIST. колумнидколумннаме</span><span class="sxs-lookup"><span data-stu-id="80d44-103">JET_INDEXLIST.columnidcolumnname property</span></span>

<span data-ttu-id="80d44-104">Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу.</span><span class="sxs-lookup"><span data-stu-id="80d44-104">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="80d44-105">См. [индекскэйгрбит](./indexkeygrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="80d44-105">See [IndexKeyGrbit](./indexkeygrbit-enumeration.md).</span></span> <span data-ttu-id="80d44-106">Столбец имеет тип [Text](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="80d44-106">The column is of type [Text](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="80d44-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="80d44-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="80d44-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="80d44-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="80d44-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80d44-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidcolumnname As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcolumnname
```

``` csharp
public JET_COLUMNID columnidcolumnname { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="80d44-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="80d44-110">Property value</span></span>

<span data-ttu-id="80d44-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="80d44-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="80d44-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80d44-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="80d44-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="80d44-113">Reference</span></span>

[<span data-ttu-id="80d44-114">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="80d44-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="80d44-115">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="80d44-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="80d44-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="80d44-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

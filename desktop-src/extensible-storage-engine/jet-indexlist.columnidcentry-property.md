---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидцентри'
title: Свойство JET_INDEXLIST. Колумнидцентри
TOCTitle: 'columnidcEntry property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcentry(v=EXCHG.10)
ms:contentKeyID: 55103597
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcEntry
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcEntry
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49f3a2a8c22a869cd70a40da72b3e2915caa638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712449"
---
# <a name="jet_indexlistcolumnidcentry-property"></a><span data-ttu-id="325bd-103">Свойство JET_INDEXLIST. Колумнидцентри</span><span class="sxs-lookup"><span data-stu-id="325bd-103">JET_INDEXLIST.columnidcEntry property</span></span>

<span data-ttu-id="325bd-104">Возвращает значение columnid столбца во временной таблице, в котором хранится количество записей в индексе.</span><span class="sxs-lookup"><span data-stu-id="325bd-104">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="325bd-105">Это значение не является текущим и обновляется только с помощью "API. Жеткомпутестатс".</span><span class="sxs-lookup"><span data-stu-id="325bd-105">This value is not current and is only is updated by "Api.JetComputeStats".</span></span> <span data-ttu-id="325bd-106">Столбец имеет тип [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="325bd-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="325bd-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="325bd-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="325bd-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="325bd-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="325bd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="325bd-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidcEntry As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcEntry
```

``` csharp
public JET_COLUMNID columnidcEntry { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="325bd-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="325bd-110">Property value</span></span>

<span data-ttu-id="325bd-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="325bd-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="325bd-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="325bd-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="325bd-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="325bd-113">Reference</span></span>

[<span data-ttu-id="325bd-114">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="325bd-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="325bd-115">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="325bd-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="325bd-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="325bd-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

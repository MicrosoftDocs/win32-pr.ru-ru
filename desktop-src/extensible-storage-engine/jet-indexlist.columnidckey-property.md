---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидккэй'
title: Свойство JET_INDEXLIST. Колумнидккэй
TOCTitle: 'columnidcKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidckey(v=EXCHG.10)
ms:contentKeyID: 55103598
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcKey
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcKey
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 884bfaaea30600919a905616cd0e808541f56ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713148"
---
# <a name="jet_indexlistcolumnidckey-property"></a><span data-ttu-id="0d7af-103">Свойство JET_INDEXLIST. Колумнидккэй</span><span class="sxs-lookup"><span data-stu-id="0d7af-103">JET_INDEXLIST.columnidcKey property</span></span>

<span data-ttu-id="0d7af-104">Возвращает значение columnid столбца во временной таблице, в котором хранится количество уникальных ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="0d7af-104">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="0d7af-105">Это значение не является текущим и обновляется только с помощью "API. Жеткомпутестатс".</span><span class="sxs-lookup"><span data-stu-id="0d7af-105">This value is not current and is only is updated by "Api.JetComputeStats".</span></span> <span data-ttu-id="0d7af-106">Столбец имеет тип [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="0d7af-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="0d7af-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d7af-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d7af-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0d7af-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d7af-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d7af-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidcKey As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcKey
```

``` csharp
public JET_COLUMNID columnidcKey { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="0d7af-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0d7af-110">Property value</span></span>

<span data-ttu-id="0d7af-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0d7af-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d7af-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d7af-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d7af-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="0d7af-113">Reference</span></span>

[<span data-ttu-id="0d7af-114">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="0d7af-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="0d7af-115">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="0d7af-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="0d7af-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0d7af-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

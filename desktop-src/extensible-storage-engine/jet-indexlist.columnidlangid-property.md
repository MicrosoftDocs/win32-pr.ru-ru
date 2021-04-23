---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидлангид'
title: Свойство JET_INDEXLIST. Колумнидлангид
TOCTitle: 'columnidLangid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLangid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidlangid(v=EXCHG.10)
ms:contentKeyID: 55103666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLangid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidLangid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLangid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidLangid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 934920cf41dd794c410588470bb694915da74469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683885"
---
# <a name="jet_indexlistcolumnidlangid-property"></a><span data-ttu-id="af798-103">Свойство JET_INDEXLIST. Колумнидлангид</span><span class="sxs-lookup"><span data-stu-id="af798-103">JET_INDEXLIST.columnidLangid property</span></span>

<span data-ttu-id="af798-104">Возвращает значение columnid столбца во временной таблице, в котором хранится идентификатор языка (LCID) индекса.</span><span class="sxs-lookup"><span data-stu-id="af798-104">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="af798-105">Столбец имеет тип [Short](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="af798-105">The column is of type [Short](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="af798-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af798-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af798-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="af798-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af798-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af798-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidLangid As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidLangid
```

``` csharp
public JET_COLUMNID columnidLangid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="af798-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="af798-109">Property value</span></span>

<span data-ttu-id="af798-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af798-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="af798-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af798-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af798-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="af798-112">Reference</span></span>

[<span data-ttu-id="af798-113">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="af798-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="af798-114">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="af798-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="af798-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="af798-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

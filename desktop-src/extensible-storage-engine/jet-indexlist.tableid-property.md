---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. TableID'
title: JET_INDEXLIST. TableID, свойство
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103670
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_tableid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_tableid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b680562a9a43162ffb82a726a410632774e39c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684302"
---
# <a name="jet_indexlisttableid-property"></a><span data-ttu-id="cd8c4-103">JET_INDEXLIST. TableID, свойство</span><span class="sxs-lookup"><span data-stu-id="cd8c4-103">JET_INDEXLIST.tableid property</span></span>

<span data-ttu-id="cd8c4-104">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-104">Gets tableid of the temporary table.</span></span> <span data-ttu-id="cd8c4-105">Этот параметр должен быть закрыт, если таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-105">This should be closed when the table is no longer needed.</span></span>

<span data-ttu-id="cd8c4-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd8c4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd8c4-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd8c4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd8c4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd8c4-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="cd8c4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cd8c4-109">Property value</span></span>

<span data-ttu-id="cd8c4-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cd8c4-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd8c4-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd8c4-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd8c4-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="cd8c4-112">Reference</span></span>

[<span data-ttu-id="cd8c4-113">Класс JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="cd8c4-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="cd8c4-114">Элементы JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="cd8c4-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="cd8c4-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cd8c4-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

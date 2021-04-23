---
description: 'Дополнительные сведения о свойстве: JET_OBJECTLIST. TableID'
title: JET_OBJECTLIST. TableID, свойство
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103778
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.set_tableid
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_OBJECTLIST.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 080d6bd1c46f86d0bb1ab780da2e44a7eb8ae6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693152"
---
# <a name="jet_objectlisttableid-property"></a><span data-ttu-id="7d002-103">JET_OBJECTLIST. TableID, свойство</span><span class="sxs-lookup"><span data-stu-id="7d002-103">JET_OBJECTLIST.tableid property</span></span>

<span data-ttu-id="7d002-104">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="7d002-104">Gets tableid of the temporary table.</span></span> <span data-ttu-id="7d002-105">Этот параметр должен быть закрыт, если таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="7d002-105">This should be closed when the table is no longer needed.</span></span>

<span data-ttu-id="7d002-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d002-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d002-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d002-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d002-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d002-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_OBJECTLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="7d002-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7d002-109">Property value</span></span>

<span data-ttu-id="7d002-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d002-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d002-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d002-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d002-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="7d002-112">Reference</span></span>

[<span data-ttu-id="7d002-113">Класс JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="7d002-113">JET_OBJECTLIST class</span></span>](./jet-objectlist-class.md)

[<span data-ttu-id="7d002-114">Элементы JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="7d002-114">JET_OBJECTLIST members</span></span>](./jet-objectlist-members.md)

[<span data-ttu-id="7d002-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7d002-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

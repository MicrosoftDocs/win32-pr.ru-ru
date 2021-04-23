---
description: 'Дополнительные сведения о свойстве: JET_COLUMNLIST. TableID'
title: JET_COLUMNLIST. TableID, свойство
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103528
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.get_tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_COLUMNLIST.set_tableid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eb1c2338fca9a1ce503033b83a9c134a08d6a9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266038"
---
# <a name="jet_columnlisttableid-property"></a><span data-ttu-id="7b629-103">JET_COLUMNLIST. TableID, свойство</span><span class="sxs-lookup"><span data-stu-id="7b629-103">JET_COLUMNLIST.tableid property</span></span>

<span data-ttu-id="7b629-104">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="7b629-104">Gets tableid of the temporary table.</span></span> <span data-ttu-id="7b629-105">Этот параметр должен быть закрыт, если таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="7b629-105">This should be closed when the table is no longer needed.</span></span>

<span data-ttu-id="7b629-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b629-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b629-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b629-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b629-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b629-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="7b629-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7b629-109">Property value</span></span>

<span data-ttu-id="7b629-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b629-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b629-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b629-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b629-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="7b629-112">Reference</span></span>

[<span data-ttu-id="7b629-113">Класс JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="7b629-113">JET_COLUMNLIST class</span></span>](./jet-columnlist-class.md)

[<span data-ttu-id="7b629-114">Элементы JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="7b629-114">JET_COLUMNLIST members</span></span>](./jet-columnlist-members.md)

[<span data-ttu-id="7b629-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7b629-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

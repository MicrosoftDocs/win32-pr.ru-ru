---
description: 'Дополнительные сведения: неявное преобразование таблицы (таблица для JET_TABLEID)'
title: Неявное преобразование таблицы (таблица для JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719606"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a><span data-ttu-id="64de3-103">Неявное преобразование таблицы (таблица для JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="64de3-103">Table Implicit conversion (Table to JET_TABLEID)</span></span>

<span data-ttu-id="64de3-104">Неявный оператор преобразования из таблицы в JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="64de3-104">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="64de3-105">Это позволяет использовать таблицу с API, которые предполагают JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="64de3-105">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span>

<span data-ttu-id="64de3-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64de3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="64de3-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64de3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64de3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64de3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a><span data-ttu-id="64de3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64de3-109">Parameters</span></span>

  - <span data-ttu-id="64de3-110">table</span><span class="sxs-lookup"><span data-stu-id="64de3-110">table</span></span>  
    <span data-ttu-id="64de3-111">Тип: [Microsoft. ISAM. ESENT. Interop. Table](./table-class.md)</span><span class="sxs-lookup"><span data-stu-id="64de3-111">Type: [Microsoft.Isam.Esent.Interop.Table](./table-class.md)</span></span>  
    
    <span data-ttu-id="64de3-112">Таблица для преобразования.</span><span class="sxs-lookup"><span data-stu-id="64de3-112">The table to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="64de3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64de3-113">Return value</span></span>

<span data-ttu-id="64de3-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="64de3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
<span data-ttu-id="64de3-115">JET_TABLEID таблицы.</span><span class="sxs-lookup"><span data-stu-id="64de3-115">The JET_TABLEID of the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="64de3-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64de3-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64de3-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="64de3-117">Reference</span></span>

[<span data-ttu-id="64de3-118">Класс Table</span><span class="sxs-lookup"><span data-stu-id="64de3-118">Table class</span></span>](./table-class.md)

[<span data-ttu-id="64de3-119">Элементы таблицы</span><span class="sxs-lookup"><span data-stu-id="64de3-119">Table members</span></span>](./table-members.md)

[<span data-ttu-id="64de3-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="64de3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

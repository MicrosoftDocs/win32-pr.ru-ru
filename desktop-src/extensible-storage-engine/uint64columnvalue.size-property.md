---
description: 'Дополнительные сведения о свойстве: UInt64ColumnValue. size'
title: UInt64ColumnValue. size, свойство
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8102b08ce8a48bb23a3618fe5829c354f200ff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910215"
---
# <a name="uint64columnvaluesize-property"></a><span data-ttu-id="c2aca-103">UInt64ColumnValue. size, свойство</span><span class="sxs-lookup"><span data-stu-id="c2aca-103">UInt64ColumnValue.Size property</span></span>

<span data-ttu-id="c2aca-104">Возвращает размер значения в столбце.</span><span class="sxs-lookup"><span data-stu-id="c2aca-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="c2aca-105">Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового).</span><span class="sxs-lookup"><span data-stu-id="c2aca-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="c2aca-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c2aca-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c2aca-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c2aca-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c2aca-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2aca-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="c2aca-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c2aca-109">Property value</span></span>

<span data-ttu-id="c2aca-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c2aca-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2aca-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2aca-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c2aca-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="c2aca-112">Reference</span></span>

[<span data-ttu-id="c2aca-113">Класс UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="c2aca-113">UInt64ColumnValue class</span></span>](./uint64columnvalue-class.md)

[<span data-ttu-id="c2aca-114">Элементы UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="c2aca-114">UInt64ColumnValue members</span></span>](./uint64columnvalue-members.md)

[<span data-ttu-id="c2aca-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c2aca-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

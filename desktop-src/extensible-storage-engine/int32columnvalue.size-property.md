---
description: 'Дополнительные сведения о свойстве: Int32ColumnValue. size'
title: Int32ColumnValue. size, свойство
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103332
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10710a8705dfaf63959c1287cae7195841a2f039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344222"
---
# <a name="int32columnvaluesize-property"></a><span data-ttu-id="b0d74-103">Int32ColumnValue. size, свойство</span><span class="sxs-lookup"><span data-stu-id="b0d74-103">Int32ColumnValue.Size property</span></span>

<span data-ttu-id="b0d74-104">Возвращает размер значения в столбце.</span><span class="sxs-lookup"><span data-stu-id="b0d74-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="b0d74-105">Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового).</span><span class="sxs-lookup"><span data-stu-id="b0d74-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="b0d74-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0d74-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b0d74-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0d74-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d74-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0d74-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="b0d74-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b0d74-109">Property value</span></span>

<span data-ttu-id="b0d74-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b0d74-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0d74-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0d74-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0d74-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="b0d74-112">Reference</span></span>

[<span data-ttu-id="b0d74-113">Класс Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="b0d74-113">Int32ColumnValue class</span></span>](./int32columnvalue-class.md)

[<span data-ttu-id="b0d74-114">Элементы Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="b0d74-114">Int32ColumnValue members</span></span>](./int32columnvalue-members.md)

[<span data-ttu-id="b0d74-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b0d74-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

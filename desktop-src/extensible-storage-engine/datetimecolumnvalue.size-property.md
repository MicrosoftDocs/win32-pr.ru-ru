---
description: 'Дополнительные сведения о свойстве: Датетимеколумнвалуе. size'
title: Датетимеколумнвалуе. size, свойство
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.datetimecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a006cafa81f46ca36d5bb76aa678122c2c6eab66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719750"
---
# <a name="datetimecolumnvaluesize-property"></a><span data-ttu-id="6b0fc-103">Датетимеколумнвалуе. size, свойство</span><span class="sxs-lookup"><span data-stu-id="6b0fc-103">DateTimeColumnValue.Size property</span></span>

<span data-ttu-id="6b0fc-104">Возвращает размер значения в столбце.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="6b0fc-105">Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового).</span><span class="sxs-lookup"><span data-stu-id="6b0fc-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="6b0fc-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b0fc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6b0fc-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6b0fc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b0fc-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="6b0fc-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6b0fc-109">Property value</span></span>

<span data-ttu-id="6b0fc-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6b0fc-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6b0fc-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b0fc-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b0fc-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="6b0fc-112">Reference</span></span>

[<span data-ttu-id="6b0fc-113">Класс Датетимеколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="6b0fc-113">DateTimeColumnValue class</span></span>](./datetimecolumnvalue-class.md)

[<span data-ttu-id="6b0fc-114">Элементы Датетимеколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="6b0fc-114">DateTimeColumnValue members</span></span>](./datetimecolumnvalue-members.md)

[<span data-ttu-id="6b0fc-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6b0fc-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

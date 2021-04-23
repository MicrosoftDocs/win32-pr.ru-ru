---
description: 'Дополнительные сведения о свойстве: Флоатколумнвалуе. size'
title: Флоатколумнвалуе. size, свойство
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103243
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.FloatColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 259701daaad1027d06bf4c28c52084dae0b062b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673465"
---
# <a name="floatcolumnvaluesize-property"></a><span data-ttu-id="4d76d-103">Флоатколумнвалуе. size, свойство</span><span class="sxs-lookup"><span data-stu-id="4d76d-103">FloatColumnValue.Size property</span></span>

<span data-ttu-id="4d76d-104">Возвращает размер значения в столбце.</span><span class="sxs-lookup"><span data-stu-id="4d76d-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="4d76d-105">Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового).</span><span class="sxs-lookup"><span data-stu-id="4d76d-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="4d76d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d76d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d76d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d76d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d76d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d76d-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="4d76d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d76d-109">Property value</span></span>

<span data-ttu-id="4d76d-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4d76d-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d76d-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d76d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d76d-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="4d76d-112">Reference</span></span>

[<span data-ttu-id="4d76d-113">Класс Флоатколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="4d76d-113">FloatColumnValue class</span></span>](./floatcolumnvalue-class.md)

[<span data-ttu-id="4d76d-114">Элементы Флоатколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="4d76d-114">FloatColumnValue members</span></span>](./floatcolumnvalue-members.md)

[<span data-ttu-id="4d76d-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4d76d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о свойстве: Битеколумнвалуе. size'
title: Битеколумнвалуе. size, свойство
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55100911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ByteColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ByteColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94679812f0bdebd043bda3596fceffad6eb2fd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719682"
---
# <a name="bytecolumnvaluesize-property"></a><span data-ttu-id="f6928-103">Битеколумнвалуе. size, свойство</span><span class="sxs-lookup"><span data-stu-id="f6928-103">ByteColumnValue.Size property</span></span>

<span data-ttu-id="f6928-104">Возвращает размер значения в столбце.</span><span class="sxs-lookup"><span data-stu-id="f6928-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="f6928-105">Он возвращает 0 для столбцов переменного размера (т. е. двоичного и строкового).</span><span class="sxs-lookup"><span data-stu-id="f6928-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="f6928-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6928-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6928-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6928-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6928-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6928-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="f6928-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f6928-109">Property value</span></span>

<span data-ttu-id="f6928-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f6928-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6928-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6928-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6928-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="f6928-112">Reference</span></span>

[<span data-ttu-id="f6928-113">Класс Битеколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="f6928-113">ByteColumnValue class</span></span>](./bytecolumnvalue-class.md)

[<span data-ttu-id="f6928-114">Элементы Битеколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="f6928-114">ByteColumnValue members</span></span>](./bytecolumnvalue-members.md)

[<span data-ttu-id="f6928-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f6928-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

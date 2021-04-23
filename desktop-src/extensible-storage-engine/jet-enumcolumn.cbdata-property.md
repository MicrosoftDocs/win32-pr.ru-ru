---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMN. cbData'
title: Свойство JET_ENUMCOLUMN. cbData
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b38d6c8433cc9792ebdd7e04e72027c6e1477e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144899"
---
# <a name="jet_enumcolumncbdata-property"></a><span data-ttu-id="a320c-103">Свойство JET_ENUMCOLUMN. cbData</span><span class="sxs-lookup"><span data-stu-id="a320c-103">JET_ENUMCOLUMN.cbData property</span></span>

<span data-ttu-id="a320c-104">Возвращает размер значения, перечисленного для столбца.</span><span class="sxs-lookup"><span data-stu-id="a320c-104">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="a320c-105">Этот элемент используется, только если [Err](./jet-enumcolumn.err-property.md) равен [колумнсинглевалуе](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="a320c-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is equal to [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="a320c-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a320c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a320c-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a320c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a320c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a320c-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cbData
```

``` csharp
public int cbData { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="a320c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a320c-109">Property value</span></span>

<span data-ttu-id="a320c-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a320c-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a320c-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a320c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a320c-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="a320c-112">Reference</span></span>

[<span data-ttu-id="a320c-113">Класс JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a320c-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="a320c-114">Элементы JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a320c-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="a320c-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a320c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMN. Ценумколумнвалуе'
title: Свойство JET_ENUMCOLUMN. Ценумколумнвалуе
TOCTitle: 'cEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103498
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee9649f7c546dee155dfcda35ece32dfe346c689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808555"
---
# <a name="jet_enumcolumncenumcolumnvalue-property"></a><span data-ttu-id="051bc-103">Свойство JET_ENUMCOLUMN. Ценумколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="051bc-103">JET_ENUMCOLUMN.cEnumColumnValue property</span></span>

<span data-ttu-id="051bc-104">Возвращает количество значений столбца, перечисленных для столбца.</span><span class="sxs-lookup"><span data-stu-id="051bc-104">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="051bc-105">Этот элемент используется только в том случае, если [Err](./jet-enumcolumn.err-property.md) не [колумнсинглевалуе](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="051bc-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is not [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="051bc-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="051bc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="051bc-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="051bc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="051bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="051bc-108">Syntax</span></span>

``` vb
'Declaration
Public Property cEnumColumnValue As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cEnumColumnValue
```

``` csharp
public int cEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="051bc-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="051bc-109">Property value</span></span>

<span data-ttu-id="051bc-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="051bc-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="051bc-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="051bc-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="051bc-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="051bc-112">Reference</span></span>

[<span data-ttu-id="051bc-113">Класс JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="051bc-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="051bc-114">Элементы JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="051bc-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="051bc-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="051bc-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

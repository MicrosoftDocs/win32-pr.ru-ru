---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMN. Рженумколумнвалуе'
title: Свойство JET_ENUMCOLUMN. Рженумколумнвалуе
TOCTitle: 'rgEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.rgenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103505
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_rgEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d0e131723ae9fb8e1f68193c96d5ed2671a74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540066"
---
# <a name="jet_enumcolumnrgenumcolumnvalue-property"></a><span data-ttu-id="8a41c-103">Свойство JET_ENUMCOLUMN. Рженумколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="8a41c-103">JET_ENUMCOLUMN.rgEnumColumnValue property</span></span>

<span data-ttu-id="8a41c-104">Возвращает перечисляемые значения столбцов для столбца.</span><span class="sxs-lookup"><span data-stu-id="8a41c-104">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="8a41c-105">Этот элемент используется только в том случае, если [Err](./jet-enumcolumn.err-property.md) не [колумнсинглевалуе](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="8a41c-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is not [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="8a41c-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8a41c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8a41c-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8a41c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8a41c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a41c-108">Syntax</span></span>

``` vb
'Declaration
Public Property rgEnumColumnValue As JET_ENUMCOLUMNVALUE()
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_ENUMCOLUMNVALUE()

value = instance.rgEnumColumnValue
```

``` csharp
public JET_ENUMCOLUMNVALUE[] rgEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8a41c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8a41c-109">Property value</span></span>

<span data-ttu-id="8a41c-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="8a41c-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a41c-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a41c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8a41c-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="8a41c-112">Reference</span></span>

[<span data-ttu-id="8a41c-113">Класс JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8a41c-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="8a41c-114">Элементы JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8a41c-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="8a41c-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8a41c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

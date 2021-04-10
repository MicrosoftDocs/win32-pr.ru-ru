---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMNVALUE. ERR'
title: Свойство JET_ENUMCOLUMNVALUE. ERR
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue.err(v=EXCHG.10)
ms:contentKeyID: 55103626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.get_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f797d82ad09b75d961be24f2382b0895880427f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266034"
---
# <a name="jet_enumcolumnvalueerr-property"></a><span data-ttu-id="6486a-103">Свойство JET_ENUMCOLUMNVALUE. ERR</span><span class="sxs-lookup"><span data-stu-id="6486a-103">JET_ENUMCOLUMNVALUE.err property</span></span>

<span data-ttu-id="6486a-104">Возвращает код состояния столбца, полученный в результате перечисления значения столбца.</span><span class="sxs-lookup"><span data-stu-id="6486a-104">Gets the column status code resulting from the enumeration of the column value.</span></span>

<span data-ttu-id="6486a-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6486a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6486a-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6486a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6486a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6486a-107">Syntax</span></span>

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="6486a-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6486a-108">Property value</span></span>

<span data-ttu-id="6486a-109">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6486a-109">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6486a-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6486a-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6486a-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="6486a-111">Reference</span></span>

[<span data-ttu-id="6486a-112">Класс JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6486a-112">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="6486a-113">Элементы JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6486a-113">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="6486a-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6486a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="6486a-115">колумннулл</span><span class="sxs-lookup"><span data-stu-id="6486a-115">ColumnNull</span></span>](./jet-wrn-enumeration.md)

[<span data-ttu-id="6486a-116">колумнскиппед</span><span class="sxs-lookup"><span data-stu-id="6486a-116">ColumnSkipped</span></span>](./jet-wrn-enumeration.md)

[<span data-ttu-id="6486a-117">колумнтрункатед</span><span class="sxs-lookup"><span data-stu-id="6486a-117">ColumnTruncated</span></span>](./jet-wrn-enumeration.md)

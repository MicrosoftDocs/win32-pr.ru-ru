---
description: 'Дополнительные сведения о свойстве: JET_COLUMNBASE. CP'
title: Свойство JET_COLUMNBASE. CP
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cp(v=EXCHG.10)
ms:contentKeyID: 55103468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8928ba3ae46283f856359b36d8f7c4c12f5891b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081596"
---
# <a name="jet_columnbasecp-property"></a><span data-ttu-id="d3798-103">Свойство JET_COLUMNBASE. CP</span><span class="sxs-lookup"><span data-stu-id="d3798-103">JET_COLUMNBASE.cp property</span></span>

<span data-ttu-id="d3798-104">Возвращает кодовую страницу столбца.</span><span class="sxs-lookup"><span data-stu-id="d3798-104">Gets code page of the column.</span></span> <span data-ttu-id="d3798-105">Это имеет смысл только для столбцов типа [Text](./jet-coltyp-enumeration.md) и [LongText](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="d3798-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md) and [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="d3798-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3798-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d3798-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d3798-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3798-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3798-108">Syntax</span></span>

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As JET_CP

value = instance.cp
```

``` csharp
public JET_CP cp { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="d3798-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d3798-109">Property value</span></span>

<span data-ttu-id="d3798-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_CP](./jet-cp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d3798-110">Type: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3798-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3798-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3798-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="d3798-112">Reference</span></span>

[<span data-ttu-id="d3798-113">Класс JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="d3798-113">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="d3798-114">Элементы JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="d3798-114">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="d3798-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d3798-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

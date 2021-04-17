---
description: 'Дополнительные сведения о свойстве: JET_COLUMNDEF. Кбмакс'
title: Свойство JET_COLUMNDEF. Кбмакс
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103491
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 486507dc046617ea6689fcf1c5eac4199cfeecd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701822"
---
# <a name="jet_columndefcbmax-property"></a><span data-ttu-id="daa2a-103">Свойство JET_COLUMNDEF. Кбмакс</span><span class="sxs-lookup"><span data-stu-id="daa2a-103">JET_COLUMNDEF.cbMax property</span></span>

<span data-ttu-id="daa2a-104">Возвращает или задает максимальную длину столбца.</span><span class="sxs-lookup"><span data-stu-id="daa2a-104">Gets or sets the maximum length of the column.</span></span> <span data-ttu-id="daa2a-105">Это имеет смысл только для столбцов типа [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [binary](./jet-coltyp-enumeration.md) и [лонгбинари](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="daa2a-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) and [LongBinary](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="daa2a-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="daa2a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="daa2a-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="daa2a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="daa2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daa2a-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="daa2a-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="daa2a-109">Property value</span></span>

<span data-ttu-id="daa2a-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="daa2a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="daa2a-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daa2a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="daa2a-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="daa2a-112">Reference</span></span>

[<span data-ttu-id="daa2a-113">Класс JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="daa2a-113">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="daa2a-114">Элементы JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="daa2a-114">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="daa2a-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="daa2a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

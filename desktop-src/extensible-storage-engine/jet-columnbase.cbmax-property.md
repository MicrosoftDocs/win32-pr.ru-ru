---
description: 'Дополнительные сведения о свойстве: JET_COLUMNBASE. Кбмакс'
title: Свойство JET_COLUMNBASE. Кбмакс
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103464
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d539df352119d24e1c8ddf7df816b8715f659417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081546"
---
# <a name="jet_columnbasecbmax-property"></a><span data-ttu-id="23491-103">Свойство JET_COLUMNBASE. Кбмакс</span><span class="sxs-lookup"><span data-stu-id="23491-103">JET_COLUMNBASE.cbMax property</span></span>

<span data-ttu-id="23491-104">Возвращает максимальную длину столбца.</span><span class="sxs-lookup"><span data-stu-id="23491-104">Gets the maximum length of the column.</span></span> <span data-ttu-id="23491-105">Это имеет смысл только для столбцов типа [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [binary](./jet-coltyp-enumeration.md) и [лонгбинари](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="23491-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) and [LongBinary](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="23491-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23491-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23491-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="23491-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23491-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23491-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As Integer

value = instance.cbMax
```

``` csharp
public int cbMax { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="23491-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="23491-109">Property value</span></span>

<span data-ttu-id="23491-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="23491-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="23491-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23491-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23491-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="23491-112">Reference</span></span>

[<span data-ttu-id="23491-113">Класс JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="23491-113">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="23491-114">Элементы JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="23491-114">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="23491-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="23491-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

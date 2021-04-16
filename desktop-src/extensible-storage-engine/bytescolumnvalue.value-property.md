---
description: См. Дополнительные сведения о свойстве Битесколумнвалуе. Value
title: Битесколумнвалуе. Value, свойство
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55107249
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0804a7a05640336be77e5f446ad99227db592f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702715"
---
# <a name="bytescolumnvaluevalue-property"></a><span data-ttu-id="ed7b3-103">Битесколумнвалуе. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="ed7b3-103">BytesColumnValue.Value property</span></span>

<span data-ttu-id="ed7b3-104">Возвращает или задает значение столбца.</span><span class="sxs-lookup"><span data-stu-id="ed7b3-104">Gets or sets the value of the column.</span></span> <span data-ttu-id="ed7b3-105">Используйте [SetColumns (JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) для обновления записи со значением столбца.</span><span class="sxs-lookup"><span data-stu-id="ed7b3-105">Use [SetColumns(JET_SESID, JET_TABLEID, \[\])](./api.setcolumns-method.md) to update a record with the column value.</span></span>

<span data-ttu-id="ed7b3-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed7b3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed7b3-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed7b3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7b3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed7b3-108">Syntax</span></span>

``` vb
'Declaration
Public Property Value As Byte()
    Get
    Set
'Usage
Dim instance As BytesColumnValue
Dim value As Byte()

value = instance.Value

instance.Value = value
```

``` csharp
public byte[] Value { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ed7b3-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ed7b3-109">Property value</span></span>

<span data-ttu-id="ed7b3-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="ed7b3-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed7b3-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed7b3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed7b3-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="ed7b3-112">Reference</span></span>

[<span data-ttu-id="ed7b3-113">Класс Битесколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="ed7b3-113">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="ed7b3-114">Элементы Битесколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="ed7b3-114">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="ed7b3-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ed7b3-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

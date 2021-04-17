---
description: См. Дополнительные сведения о свойстве Стрингколумнвалуе. Value
title: Стрингколумнвалуе. Value, свойство
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55104098
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b1f5dc65f41e1714858c75bed2c22e23680b60cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693618"
---
# <a name="stringcolumnvaluevalue-property"></a><span data-ttu-id="0c54e-103">Стрингколумнвалуе. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="0c54e-103">StringColumnValue.Value property</span></span>

<span data-ttu-id="0c54e-104">Возвращает или задает значение столбца.</span><span class="sxs-lookup"><span data-stu-id="0c54e-104">Gets or sets the value of the column.</span></span> <span data-ttu-id="0c54e-105">Используйте [SetColumns (JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) для обновления записи со значением столбца.</span><span class="sxs-lookup"><span data-stu-id="0c54e-105">Use [SetColumns(JET_SESID, JET_TABLEID, \[\])](./api.setcolumns-method.md) to update a record with the column value.</span></span>

<span data-ttu-id="0c54e-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c54e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c54e-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c54e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c54e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c54e-108">Syntax</span></span>

``` vb
'Declaration
Public Property Value As String
    Get
    Set
'Usage
Dim instance As StringColumnValue
Dim value As String

value = instance.Value

instance.Value = value
```

``` csharp
public string Value { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0c54e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0c54e-109">Property value</span></span>

<span data-ttu-id="0c54e-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0c54e-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c54e-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c54e-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c54e-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="0c54e-112">Reference</span></span>

[<span data-ttu-id="0c54e-113">Класс Стрингколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="0c54e-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="0c54e-114">Элементы Стрингколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="0c54e-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="0c54e-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0c54e-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMNID. columnid'
title: Свойство JET_ENUMCOLUMNID. columnid
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1c456a4eb208ba8c9f2ac39ea0b4dad410ee270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143600"
---
# <a name="jet_enumcolumnidcolumnid-property"></a><span data-ttu-id="99113-103">Свойство JET_ENUMCOLUMNID. columnid</span><span class="sxs-lookup"><span data-stu-id="99113-103">JET_ENUMCOLUMNID.columnid property</span></span>

<span data-ttu-id="99113-104">Возвращает или задает идентификатор columnid для перечисления.</span><span class="sxs-lookup"><span data-stu-id="99113-104">Gets or sets the columnid ID to enumerate.</span></span>

<span data-ttu-id="99113-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99113-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99113-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99113-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99113-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99113-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="99113-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="99113-108">Property value</span></span>

<span data-ttu-id="99113-109">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="99113-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="remarks"></a><span data-ttu-id="99113-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99113-110">Remarks</span></span>

<span data-ttu-id="99113-111">Если идентификатор столбца равен 0 (нулю), то перечисление этого столбца пропускается, а соответствующая область в выходном массиве JET_ENUMCOLUMN структур будет создана с состоянием столбца JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="99113-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of JET_ENUMCOLUMN structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

## <a name="see-also"></a><span data-ttu-id="99113-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99113-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99113-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="99113-113">Reference</span></span>

[<span data-ttu-id="99113-114">Класс JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="99113-114">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="99113-115">Элементы JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="99113-115">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="99113-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="99113-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

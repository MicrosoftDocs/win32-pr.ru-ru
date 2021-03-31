---
description: Дополнительные сведения о методе API. SetColumns
title: API. SetColumns, метод
TOCTitle: 'SetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ColumnValue[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumns(v=EXCHG.10)
ms:contentKeyID: 55100936
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4ed75c668c0000c1d01d521a57ead46055bc8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808255"
---
# <a name="apisetcolumns-method"></a><span data-ttu-id="04248-103">API. SetColumns, метод</span><span class="sxs-lookup"><span data-stu-id="04248-103">Api.SetColumns method</span></span>

<span data-ttu-id="04248-104">Задает столбцы из объектов Колумнвалуе.</span><span class="sxs-lookup"><span data-stu-id="04248-104">Sets columns from ColumnValue objects.</span></span>

<span data-ttu-id="04248-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04248-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04248-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="04248-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04248-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04248-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ParamArray values As ColumnValue() _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim values As ColumnValue()

Api.SetColumns(sesid, tableid, values)
```

``` csharp
public static void SetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    params ColumnValue[] values
)
```

#### <a name="parameters"></a><span data-ttu-id="04248-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="04248-108">Parameters</span></span>

  - <span data-ttu-id="04248-109">сесид</span><span class="sxs-lookup"><span data-stu-id="04248-109">sesid</span></span>  
    <span data-ttu-id="04248-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04248-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="04248-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="04248-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="04248-112">TableID</span><span class="sxs-lookup"><span data-stu-id="04248-112">tableid</span></span>  
    <span data-ttu-id="04248-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04248-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="04248-114">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="04248-114">The cursor to update.</span></span> <span data-ttu-id="04248-115">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="04248-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="04248-116">значения</span><span class="sxs-lookup"><span data-stu-id="04248-116">values</span></span>  
    <span data-ttu-id="04248-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="04248-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="04248-118">Заданные значения.</span><span class="sxs-lookup"><span data-stu-id="04248-118">The values to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="04248-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04248-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04248-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="04248-120">Reference</span></span>

[<span data-ttu-id="04248-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="04248-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="04248-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="04248-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="04248-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="04248-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

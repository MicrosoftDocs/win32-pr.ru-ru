---
description: Дополнительные сведения о методе API. Жетаддколумн
title: API. Жетаддколумн, метод
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a864bab9c3b888622640e6226c3e7ee542a096d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701427"
---
# <a name="apijetaddcolumn-method"></a><span data-ttu-id="a58df-103">API. Жетаддколумн, метод</span><span class="sxs-lookup"><span data-stu-id="a58df-103">Api.JetAddColumn method</span></span>

<span data-ttu-id="a58df-104">Добавить новый столбец в существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a58df-104">Add a new column to an existing table.</span></span>

<span data-ttu-id="a58df-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a58df-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a58df-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a58df-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a58df-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a58df-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="a58df-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a58df-108">Parameters</span></span>

  - <span data-ttu-id="a58df-109">сесид</span><span class="sxs-lookup"><span data-stu-id="a58df-109">sesid</span></span>  
    <span data-ttu-id="a58df-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a58df-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a58df-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a58df-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a58df-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a58df-112">tableid</span></span>  
    <span data-ttu-id="a58df-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a58df-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a58df-114">Таблица, в которую добавляется столбец.</span><span class="sxs-lookup"><span data-stu-id="a58df-114">The table to add the column to.</span></span>

<!-- end list -->

  - <span data-ttu-id="a58df-115">столбец</span><span class="sxs-lookup"><span data-stu-id="a58df-115">column</span></span>  
    <span data-ttu-id="a58df-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a58df-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a58df-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="a58df-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a58df-118">колумндеф</span><span class="sxs-lookup"><span data-stu-id="a58df-118">columndef</span></span>  
    <span data-ttu-id="a58df-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="a58df-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="a58df-120">Определение столбца.</span><span class="sxs-lookup"><span data-stu-id="a58df-120">The definition of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a58df-121">defaultValue</span><span class="sxs-lookup"><span data-stu-id="a58df-121">defaultValue</span></span>  
    <span data-ttu-id="a58df-122">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="a58df-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="a58df-123">Значение по умолчанию для столбца.</span><span class="sxs-lookup"><span data-stu-id="a58df-123">The default value of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a58df-124">дефаултвалуесизе</span><span class="sxs-lookup"><span data-stu-id="a58df-124">defaultValueSize</span></span>  
    <span data-ttu-id="a58df-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a58df-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a58df-126">Размер значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a58df-126">The size of the default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="a58df-127">columnid</span><span class="sxs-lookup"><span data-stu-id="a58df-127">columnid</span></span>  
    <span data-ttu-id="a58df-128">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a58df-128">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="a58df-129">Возвращает значение columnid нового столбца.</span><span class="sxs-lookup"><span data-stu-id="a58df-129">Returns the columnid of the new column.</span></span>

## <a name="see-also"></a><span data-ttu-id="a58df-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a58df-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a58df-131">Справочник</span><span class="sxs-lookup"><span data-stu-id="a58df-131">Reference</span></span>

[<span data-ttu-id="a58df-132">Класс API</span><span class="sxs-lookup"><span data-stu-id="a58df-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a58df-133">Члены API</span><span class="sxs-lookup"><span data-stu-id="a58df-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a58df-134">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a58df-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

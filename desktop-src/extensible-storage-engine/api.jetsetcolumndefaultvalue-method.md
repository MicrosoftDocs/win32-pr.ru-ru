---
description: Дополнительные сведения о методе API. Жетсетколумндефаултвалуе
title: API. Жетсетколумндефаултвалуе, метод
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703245"
---
# <a name="apijetsetcolumndefaultvalue-method"></a><span data-ttu-id="c659f-103">API. Жетсетколумндефаултвалуе, метод</span><span class="sxs-lookup"><span data-stu-id="c659f-103">Api.JetSetColumnDefaultValue method</span></span>

<span data-ttu-id="c659f-104">Изменяет значение существующего столбца по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c659f-104">Changes the default value of an existing column.</span></span>

<span data-ttu-id="c659f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c659f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c659f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c659f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c659f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c659f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c659f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c659f-108">Parameters</span></span>

  - <span data-ttu-id="c659f-109">сесид</span><span class="sxs-lookup"><span data-stu-id="c659f-109">sesid</span></span>  
    <span data-ttu-id="c659f-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c659f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c659f-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c659f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c659f-112">dbid</span><span class="sxs-lookup"><span data-stu-id="c659f-112">dbid</span></span>  
    <span data-ttu-id="c659f-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c659f-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c659f-114">База данных, содержащая столбец.</span><span class="sxs-lookup"><span data-stu-id="c659f-114">The database containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="c659f-115">tableName</span><span class="sxs-lookup"><span data-stu-id="c659f-115">tableName</span></span>  
    <span data-ttu-id="c659f-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c659f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c659f-117">Имя таблицы, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="c659f-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="c659f-118">columnName</span><span class="sxs-lookup"><span data-stu-id="c659f-118">columnName</span></span>  
    <span data-ttu-id="c659f-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c659f-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c659f-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="c659f-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="c659f-121">.</span><span class="sxs-lookup"><span data-stu-id="c659f-121">data</span></span>  
    <span data-ttu-id="c659f-122">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="c659f-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="c659f-123">Новое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c659f-123">The new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="c659f-124">dataSize</span><span class="sxs-lookup"><span data-stu-id="c659f-124">dataSize</span></span>  
    <span data-ttu-id="c659f-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c659f-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c659f-126">Размер нового значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c659f-126">Size of the new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="c659f-127">грбит</span><span class="sxs-lookup"><span data-stu-id="c659f-127">grbit</span></span>  
    <span data-ttu-id="c659f-128">Тип: [Microsoft. ISAM. ESENT. Interop. сетколумндефаултвалуегрбит](./setcolumndefaultvaluegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c659f-128">Type: [Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c659f-129">Параметры значения по умолчанию для столбца.</span><span class="sxs-lookup"><span data-stu-id="c659f-129">Column default value options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c659f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c659f-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c659f-131">Справочник</span><span class="sxs-lookup"><span data-stu-id="c659f-131">Reference</span></span>

[<span data-ttu-id="c659f-132">Класс API</span><span class="sxs-lookup"><span data-stu-id="c659f-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c659f-133">Члены API</span><span class="sxs-lookup"><span data-stu-id="c659f-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c659f-134">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c659f-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения: метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)'
title: Метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100705
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e690dbb2a4b82698440b3be3c483bb46b2eca8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897006"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnbase"></a><span data-ttu-id="a7d38-103">Метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)</span><span class="sxs-lookup"><span data-stu-id="a7d38-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</span></span>

<span data-ttu-id="a7d38-104">Извлекает сведения о столбце в таблице.</span><span class="sxs-lookup"><span data-stu-id="a7d38-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="a7d38-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7d38-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a7d38-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7d38-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d38-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7d38-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnbase As JET_COLUMNBASEApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="a7d38-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7d38-108">Parameters</span></span>

  - <span data-ttu-id="a7d38-109">сесид</span><span class="sxs-lookup"><span data-stu-id="a7d38-109">sesid</span></span>  
    <span data-ttu-id="a7d38-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7d38-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a7d38-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a7d38-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7d38-112">dbid</span><span class="sxs-lookup"><span data-stu-id="a7d38-112">dbid</span></span>  
    <span data-ttu-id="a7d38-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7d38-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a7d38-114">База данных, содержащая таблицу.</span><span class="sxs-lookup"><span data-stu-id="a7d38-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7d38-115">tablename</span><span class="sxs-lookup"><span data-stu-id="a7d38-115">tablename</span></span>  
    <span data-ttu-id="a7d38-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a7d38-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a7d38-117">Имя таблицы, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="a7d38-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7d38-118">columnName</span><span class="sxs-lookup"><span data-stu-id="a7d38-118">columnName</span></span>  
    <span data-ttu-id="a7d38-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a7d38-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a7d38-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="a7d38-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7d38-121">колумнбасе</span><span class="sxs-lookup"><span data-stu-id="a7d38-121">columnbase</span></span>  
    <span data-ttu-id="a7d38-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="a7d38-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="a7d38-123">Заполняется сведениями о столбцах в таблице.</span><span class="sxs-lookup"><span data-stu-id="a7d38-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7d38-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7d38-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7d38-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="a7d38-125">Reference</span></span>

[<span data-ttu-id="a7d38-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="a7d38-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a7d38-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="a7d38-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a7d38-128">Перегрузка Жетжетколумнинфо</span><span class="sxs-lookup"><span data-stu-id="a7d38-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="a7d38-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a7d38-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения: метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNDEF)'
title: Метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNDEF)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4af99e7cfdc9f2f1fe83095ad92797ce0b34bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144332"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a><span data-ttu-id="6f33d-103">Метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="6f33d-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="6f33d-104">Извлекает сведения о столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f33d-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="6f33d-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f33d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f33d-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6f33d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f33d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f33d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="6f33d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f33d-108">Parameters</span></span>

  - <span data-ttu-id="6f33d-109">сесид</span><span class="sxs-lookup"><span data-stu-id="6f33d-109">sesid</span></span>  
    <span data-ttu-id="6f33d-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6f33d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6f33d-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="6f33d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f33d-112">dbid</span><span class="sxs-lookup"><span data-stu-id="6f33d-112">dbid</span></span>  
    <span data-ttu-id="6f33d-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6f33d-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6f33d-114">База данных, содержащая таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f33d-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f33d-115">tablename</span><span class="sxs-lookup"><span data-stu-id="6f33d-115">tablename</span></span>  
    <span data-ttu-id="6f33d-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6f33d-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6f33d-117">Имя таблицы, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="6f33d-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f33d-118">columnName</span><span class="sxs-lookup"><span data-stu-id="6f33d-118">columnName</span></span>  
    <span data-ttu-id="6f33d-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6f33d-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6f33d-120">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="6f33d-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f33d-121">колумндеф</span><span class="sxs-lookup"><span data-stu-id="6f33d-121">columndef</span></span>  
    <span data-ttu-id="6f33d-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="6f33d-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="6f33d-123">Заполняется сведениями о столбце.</span><span class="sxs-lookup"><span data-stu-id="6f33d-123">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f33d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f33d-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f33d-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="6f33d-125">Reference</span></span>

[<span data-ttu-id="6f33d-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="6f33d-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6f33d-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="6f33d-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6f33d-128">Перегрузка Жетжетколумнинфо</span><span class="sxs-lookup"><span data-stu-id="6f33d-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="6f33d-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6f33d-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

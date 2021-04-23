---
description: 'Дополнительные сведения: метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)'
title: Метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100724
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60e984fdb1577dc69a352c327c1af605e0d441d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344252"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columndef"></a><span data-ttu-id="d4809-103">Метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="d4809-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="d4809-104">Извлекает сведения о столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4809-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="d4809-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d4809-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d4809-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d4809-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d4809-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4809-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="d4809-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4809-108">Parameters</span></span>

  - <span data-ttu-id="d4809-109">сесид</span><span class="sxs-lookup"><span data-stu-id="d4809-109">sesid</span></span>  
    <span data-ttu-id="d4809-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4809-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d4809-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d4809-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4809-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d4809-112">tableid</span></span>  
    <span data-ttu-id="d4809-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4809-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d4809-114">Таблица, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="d4809-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4809-115">columnName</span><span class="sxs-lookup"><span data-stu-id="d4809-115">columnName</span></span>  
    <span data-ttu-id="d4809-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d4809-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d4809-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="d4809-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4809-118">колумндеф</span><span class="sxs-lookup"><span data-stu-id="d4809-118">columndef</span></span>  
    <span data-ttu-id="d4809-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="d4809-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="d4809-120">Заполняется сведениями о столбце.</span><span class="sxs-lookup"><span data-stu-id="d4809-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4809-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4809-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d4809-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="d4809-122">Reference</span></span>

[<span data-ttu-id="d4809-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="d4809-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d4809-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="d4809-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d4809-125">Перегрузка Жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="d4809-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="d4809-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d4809-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

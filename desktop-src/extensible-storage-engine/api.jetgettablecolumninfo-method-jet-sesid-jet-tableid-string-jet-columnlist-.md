---
description: 'Дополнительные сведения: метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)'
title: Метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100723
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
ms.openlocfilehash: 516dad3bbc93a12ec216c5c3caa35617ea989bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817001"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columnlist"></a><span data-ttu-id="f28ce-103">Метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</span><span class="sxs-lookup"><span data-stu-id="f28ce-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="f28ce-104">Извлекает сведения обо всех столбцах в таблице.</span><span class="sxs-lookup"><span data-stu-id="f28ce-104">Retrieves information about all columns in the table.</span></span>

<span data-ttu-id="f28ce-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f28ce-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f28ce-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f28ce-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f28ce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f28ce-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columnlist)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="f28ce-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f28ce-108">Parameters</span></span>

  - <span data-ttu-id="f28ce-109">сесид</span><span class="sxs-lookup"><span data-stu-id="f28ce-109">sesid</span></span>  
    <span data-ttu-id="f28ce-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f28ce-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f28ce-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="f28ce-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f28ce-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f28ce-112">tableid</span></span>  
    <span data-ttu-id="f28ce-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f28ce-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f28ce-114">Таблица, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="f28ce-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f28ce-115">columnName</span><span class="sxs-lookup"><span data-stu-id="f28ce-115">columnName</span></span>  
    <span data-ttu-id="f28ce-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f28ce-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f28ce-117">Параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f28ce-117">The parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="f28ce-118">колумнлист</span><span class="sxs-lookup"><span data-stu-id="f28ce-118">columnlist</span></span>  
    <span data-ttu-id="f28ce-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="f28ce-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="f28ce-120">Заполняется сведениями о столбцах в таблице.</span><span class="sxs-lookup"><span data-stu-id="f28ce-120">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="f28ce-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f28ce-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f28ce-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="f28ce-122">Reference</span></span>

[<span data-ttu-id="f28ce-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="f28ce-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f28ce-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="f28ce-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f28ce-125">Перегрузка Жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="f28ce-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="f28ce-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f28ce-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

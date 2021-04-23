---
description: 'Дополнительные сведения: метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)'
title: Метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100730
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa120cf78001ed608a2385e07f388ae91bc9b425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817008"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-jet_columnid-jet_columndef"></a><span data-ttu-id="76375-103">Метод API. Жетжеттаблеколумнинфо (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="76375-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span></span>

<span data-ttu-id="76375-104">Извлекает сведения о столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="76375-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="76375-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76375-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76375-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="76375-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76375-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76375-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnid, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="76375-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76375-108">Parameters</span></span>

  - <span data-ttu-id="76375-109">сесид</span><span class="sxs-lookup"><span data-stu-id="76375-109">sesid</span></span>  
    <span data-ttu-id="76375-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76375-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="76375-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="76375-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="76375-112">TableID</span><span class="sxs-lookup"><span data-stu-id="76375-112">tableid</span></span>  
    <span data-ttu-id="76375-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76375-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="76375-114">Таблица, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="76375-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="76375-115">columnid</span><span class="sxs-lookup"><span data-stu-id="76375-115">columnid</span></span>  
    <span data-ttu-id="76375-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76375-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="76375-117">Значение columnid столбца.</span><span class="sxs-lookup"><span data-stu-id="76375-117">The columnid of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="76375-118">колумндеф</span><span class="sxs-lookup"><span data-stu-id="76375-118">columndef</span></span>  
    <span data-ttu-id="76375-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="76375-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="76375-120">Заполняется сведениями о столбце.</span><span class="sxs-lookup"><span data-stu-id="76375-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="76375-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76375-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76375-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="76375-122">Reference</span></span>

[<span data-ttu-id="76375-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="76375-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="76375-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="76375-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="76375-125">Перегрузка Жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="76375-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="76375-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="76375-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

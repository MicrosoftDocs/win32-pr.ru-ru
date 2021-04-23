---
description: Дополнительные сведения о методе API. JetDeleteColumn2
title: API. JetDeleteColumn2, метод
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710953"
---
# <a name="apijetdeletecolumn2-method"></a><span data-ttu-id="dc6dd-103">API. JetDeleteColumn2, метод</span><span class="sxs-lookup"><span data-stu-id="dc6dd-103">Api.JetDeleteColumn2 method</span></span>

<span data-ttu-id="dc6dd-104">Удаляет столбец из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc6dd-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="dc6dd-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc6dd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc6dd-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc6dd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6dd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc6dd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dc6dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc6dd-108">Parameters</span></span>

  - <span data-ttu-id="dc6dd-109">сесид</span><span class="sxs-lookup"><span data-stu-id="dc6dd-109">sesid</span></span>  
    <span data-ttu-id="dc6dd-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc6dd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dc6dd-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="dc6dd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc6dd-112">TableID</span><span class="sxs-lookup"><span data-stu-id="dc6dd-112">tableid</span></span>  
    <span data-ttu-id="dc6dd-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc6dd-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dc6dd-114">Курсор на таблице, из которого удаляется столбец.</span><span class="sxs-lookup"><span data-stu-id="dc6dd-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc6dd-115">столбец</span><span class="sxs-lookup"><span data-stu-id="dc6dd-115">column</span></span>  
    <span data-ttu-id="dc6dd-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dc6dd-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="dc6dd-117">Имя удаляемого столбца.</span><span class="sxs-lookup"><span data-stu-id="dc6dd-117">The name of the column to be deleted.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc6dd-118">грбит</span><span class="sxs-lookup"><span data-stu-id="dc6dd-118">grbit</span></span>  
    <span data-ttu-id="dc6dd-119">Тип: [Microsoft. ISAM. ESENT. Interop. делетеколумнгрбит](./deletecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dc6dd-119">Type: [Microsoft.Isam.Esent.Interop.DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dc6dd-120">Параметры удаления столбцов.</span><span class="sxs-lookup"><span data-stu-id="dc6dd-120">Column deletion options.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc6dd-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc6dd-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc6dd-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="dc6dd-122">Reference</span></span>

[<span data-ttu-id="dc6dd-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="dc6dd-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dc6dd-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="dc6dd-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dc6dd-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dc6dd-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

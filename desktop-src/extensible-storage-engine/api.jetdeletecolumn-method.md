---
description: Дополнительные сведения о методе API. Жетделетеколумн
title: API. Жетделетеколумн, метод
TOCTitle: 'JetDeleteColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn(v=EXCHG.10)
ms:contentKeyID: 55100684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0801ffae0429b0c1d16d452d4170bdc6ce74937f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144353"
---
# <a name="apijetdeletecolumn-method"></a><span data-ttu-id="d9483-103">API. Жетделетеколумн, метод</span><span class="sxs-lookup"><span data-stu-id="d9483-103">Api.JetDeleteColumn method</span></span>

<span data-ttu-id="d9483-104">Удаляет столбец из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="d9483-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="d9483-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9483-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9483-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9483-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9483-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9483-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As StringApi.JetDeleteColumn(sesid, tableid, _
    column)
```

``` csharp
public static void JetDeleteColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column
)
```

#### <a name="parameters"></a><span data-ttu-id="d9483-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9483-108">Parameters</span></span>

  - <span data-ttu-id="d9483-109">сесид</span><span class="sxs-lookup"><span data-stu-id="d9483-109">sesid</span></span>  
    <span data-ttu-id="d9483-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d9483-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d9483-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d9483-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d9483-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d9483-112">tableid</span></span>  
    <span data-ttu-id="d9483-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d9483-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d9483-114">Курсор на таблице, из которого удаляется столбец.</span><span class="sxs-lookup"><span data-stu-id="d9483-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d9483-115">столбец</span><span class="sxs-lookup"><span data-stu-id="d9483-115">column</span></span>  
    <span data-ttu-id="d9483-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d9483-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d9483-117">Имя удаляемого столбца.</span><span class="sxs-lookup"><span data-stu-id="d9483-117">The name of the column to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9483-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9483-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9483-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="d9483-119">Reference</span></span>

[<span data-ttu-id="d9483-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="d9483-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d9483-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="d9483-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d9483-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d9483-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения: Конструктор таблиц'
title: Конструктор таблиц
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692494"
---
# <a name="table-constructor"></a><span data-ttu-id="7e903-103">Конструктор таблиц</span><span class="sxs-lookup"><span data-stu-id="7e903-103">Table constructor</span></span>

<span data-ttu-id="7e903-104">Инициализирует новый экземпляр класса Table.</span><span class="sxs-lookup"><span data-stu-id="7e903-104">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="7e903-105">Таблица открывается из заданной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e903-105">The table is opened from the given database.</span></span>

<span data-ttu-id="7e903-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e903-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e903-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e903-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e903-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e903-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7e903-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e903-109">Parameters</span></span>

  - <span data-ttu-id="7e903-110">сесид</span><span class="sxs-lookup"><span data-stu-id="7e903-110">sesid</span></span>  
    <span data-ttu-id="7e903-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e903-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e903-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="7e903-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e903-113">dbid</span><span class="sxs-lookup"><span data-stu-id="7e903-113">dbid</span></span>  
    <span data-ttu-id="7e903-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e903-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7e903-115">База данных, в которой будет открыта таблица.</span><span class="sxs-lookup"><span data-stu-id="7e903-115">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e903-116">name</span><span class="sxs-lookup"><span data-stu-id="7e903-116">name</span></span>  
    <span data-ttu-id="7e903-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7e903-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7e903-118">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="7e903-118">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e903-119">грбит</span><span class="sxs-lookup"><span data-stu-id="7e903-119">grbit</span></span>  
    <span data-ttu-id="7e903-120">Тип: [Microsoft. ISAM. ESENT. Interop. опентаблегрбит](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7e903-120">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7e903-121">Параметры Жетопентабле.</span><span class="sxs-lookup"><span data-stu-id="7e903-121">JetOpenTable options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e903-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e903-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e903-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="7e903-123">Reference</span></span>

[<span data-ttu-id="7e903-124">Класс Table</span><span class="sxs-lookup"><span data-stu-id="7e903-124">Table class</span></span>](./table-class.md)

[<span data-ttu-id="7e903-125">Элементы таблицы</span><span class="sxs-lookup"><span data-stu-id="7e903-125">Table members</span></span>](./table-members.md)

[<span data-ttu-id="7e903-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7e903-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о методе: Вистаапи. Жетжетколумнинфо'
title: Вистаапи. Жетжетколумнинфо, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154547"
---
# <a name="vistaapijetgetcolumninfo-method"></a><span data-ttu-id="ee4df-103">Вистаапи. Жетжетколумнинфо, метод</span><span class="sxs-lookup"><span data-stu-id="ee4df-103">VistaApi.JetGetColumnInfo method</span></span>

<span data-ttu-id="ee4df-104">Извлекает сведения о столбце в таблице.</span><span class="sxs-lookup"><span data-stu-id="ee4df-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="ee4df-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee4df-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ee4df-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee4df-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4df-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee4df-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="ee4df-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee4df-108">Parameters</span></span>

  - <span data-ttu-id="ee4df-109">сесид</span><span class="sxs-lookup"><span data-stu-id="ee4df-109">sesid</span></span>  
    <span data-ttu-id="ee4df-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee4df-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ee4df-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="ee4df-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee4df-112">dbid</span><span class="sxs-lookup"><span data-stu-id="ee4df-112">dbid</span></span>  
    <span data-ttu-id="ee4df-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee4df-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="ee4df-114">База данных, содержащая таблицу.</span><span class="sxs-lookup"><span data-stu-id="ee4df-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee4df-115">tablename</span><span class="sxs-lookup"><span data-stu-id="ee4df-115">tablename</span></span>  
    <span data-ttu-id="ee4df-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ee4df-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ee4df-117">Имя таблицы, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="ee4df-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee4df-118">columnid</span><span class="sxs-lookup"><span data-stu-id="ee4df-118">columnid</span></span>  
    <span data-ttu-id="ee4df-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee4df-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ee4df-120">Идентификатор столбца.</span><span class="sxs-lookup"><span data-stu-id="ee4df-120">The ID of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee4df-121">колумнбасе</span><span class="sxs-lookup"><span data-stu-id="ee4df-121">columnbase</span></span>  
    <span data-ttu-id="ee4df-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="ee4df-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="ee4df-123">Заполняется сведениями о столбцах в таблице.</span><span class="sxs-lookup"><span data-stu-id="ee4df-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee4df-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee4df-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee4df-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="ee4df-125">Reference</span></span>

[<span data-ttu-id="ee4df-126">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="ee4df-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="ee4df-127">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="ee4df-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="ee4df-128">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="ee4df-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

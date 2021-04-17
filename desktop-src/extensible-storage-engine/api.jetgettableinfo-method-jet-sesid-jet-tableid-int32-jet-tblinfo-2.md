---
description: 'Дополнительные сведения: метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)'
title: Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32 , JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32[],Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100746
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1706fc554eedd4a8a9365263b93c5763fb350a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711338"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-int32--jet_tblinfo"></a><span data-ttu-id="f97b7-103">Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="f97b7-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32 , JET_TblInfo)</span></span>

<span data-ttu-id="f97b7-104">Извлекает различные фрагменты информации о таблице в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f97b7-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="f97b7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f97b7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f97b7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f97b7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f97b7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f97b7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    result As Integer(), _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As Integer()
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int[] result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="f97b7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f97b7-108">Parameters</span></span>

  - <span data-ttu-id="f97b7-109">сесид</span><span class="sxs-lookup"><span data-stu-id="f97b7-109">sesid</span></span>  
    <span data-ttu-id="f97b7-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f97b7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f97b7-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="f97b7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f97b7-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f97b7-112">tableid</span></span>  
    <span data-ttu-id="f97b7-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f97b7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f97b7-114">Таблица, сведения о которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="f97b7-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="f97b7-115">result</span><span class="sxs-lookup"><span data-stu-id="f97b7-115">result</span></span>  
    <span data-ttu-id="f97b7-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="f97b7-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="f97b7-117">Извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="f97b7-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="f97b7-118">инфолевел</span><span class="sxs-lookup"><span data-stu-id="f97b7-118">infoLevel</span></span>  
    <span data-ttu-id="f97b7-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f97b7-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="f97b7-120">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="f97b7-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="f97b7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f97b7-121">Remarks</span></span>

<span data-ttu-id="f97b7-122">Эта перегрузка используется с [спацеусаже](./jet-tblinfo-enumeration.md) и [спацеаллок](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f97b7-122">This overload is used with [SpaceUsage](./jet-tblinfo-enumeration.md) and [SpaceAlloc](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f97b7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f97b7-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f97b7-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="f97b7-124">Reference</span></span>

[<span data-ttu-id="f97b7-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="f97b7-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f97b7-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="f97b7-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f97b7-127">Перегрузка Жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="f97b7-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="f97b7-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f97b7-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

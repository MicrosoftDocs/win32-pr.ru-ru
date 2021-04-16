---
description: 'Дополнительные сведения: метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)'
title: Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100736
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
ms.openlocfilehash: e955a1b854162bd8eca4e19506329c2cf6016e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712662"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_dbid-jet_tblinfo"></a><span data-ttu-id="7f289-103">Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="7f289-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</span></span>

<span data-ttu-id="7f289-104">Извлекает различные фрагменты информации о таблице в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7f289-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="7f289-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f289-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f289-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f289-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f289-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f289-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_DBID, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_DBID
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_DBID result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="7f289-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f289-108">Parameters</span></span>

  - <span data-ttu-id="7f289-109">сесид</span><span class="sxs-lookup"><span data-stu-id="7f289-109">sesid</span></span>  
    <span data-ttu-id="7f289-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7f289-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7f289-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="7f289-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f289-112">TableID</span><span class="sxs-lookup"><span data-stu-id="7f289-112">tableid</span></span>  
    <span data-ttu-id="7f289-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7f289-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7f289-114">Таблица, сведения о которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="7f289-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f289-115">result</span><span class="sxs-lookup"><span data-stu-id="7f289-115">result</span></span>  
    <span data-ttu-id="7f289-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7f289-116">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7f289-117">Извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="7f289-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f289-118">инфолевел</span><span class="sxs-lookup"><span data-stu-id="7f289-118">infoLevel</span></span>  
    <span data-ttu-id="7f289-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7f289-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="7f289-120">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="7f289-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f289-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f289-121">Remarks</span></span>

<span data-ttu-id="7f289-122">Эта перегрузка используется с [DBID](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="7f289-122">This overload is used with [Dbid](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7f289-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f289-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f289-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="7f289-124">Reference</span></span>

[<span data-ttu-id="7f289-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="7f289-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7f289-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="7f289-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7f289-127">Перегрузка Жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="7f289-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="7f289-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7f289-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

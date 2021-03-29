---
description: 'Дополнительные сведения: метод API. Жетжетобжектинфо (JET_SESID, JET_DBID, JET_OBJECTLIST)'
title: Метод API. Жетжетобжектинфо (JET_SESID, JET_DBID, JET_OBJECTLIST)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_OBJECTLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_OBJECTLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100728
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9564b0eb2dc8a5bee2e65b729164f39a19d349fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809221"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objectlist"></a><span data-ttu-id="29322-103">Метод API. Жетжетобжектинфо (JET_SESID, JET_DBID, JET_OBJECTLIST)</span><span class="sxs-lookup"><span data-stu-id="29322-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_OBJECTLIST)</span></span>

<span data-ttu-id="29322-104">Извлекает сведения об объектах базы данных.</span><span class="sxs-lookup"><span data-stu-id="29322-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="29322-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="29322-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="29322-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="29322-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="29322-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29322-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef objectlist As JET_OBJECTLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objectlist As JET_OBJECTLISTApi.JetGetObjectInfo(sesid, dbid, _
    objectlist)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out JET_OBJECTLIST objectlist
)
```

#### <a name="parameters"></a><span data-ttu-id="29322-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="29322-108">Parameters</span></span>

  - <span data-ttu-id="29322-109">сесид</span><span class="sxs-lookup"><span data-stu-id="29322-109">sesid</span></span>  
    <span data-ttu-id="29322-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29322-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="29322-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="29322-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="29322-112">dbid</span><span class="sxs-lookup"><span data-stu-id="29322-112">dbid</span></span>  
    <span data-ttu-id="29322-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="29322-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="29322-114">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="29322-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="29322-115">ObjectList</span><span class="sxs-lookup"><span data-stu-id="29322-115">objectlist</span></span>  
    <span data-ttu-id="29322-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTLIST](./jet-objectlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="29322-116">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTLIST](./jet-objectlist-class.md)</span></span>  
    
    <span data-ttu-id="29322-117">Заполняется сведениями об объектах в базе данных.</span><span class="sxs-lookup"><span data-stu-id="29322-117">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="29322-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29322-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="29322-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="29322-119">Reference</span></span>

[<span data-ttu-id="29322-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="29322-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="29322-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="29322-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="29322-122">Перегрузка Жетжетобжектинфо</span><span class="sxs-lookup"><span data-stu-id="29322-122">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="29322-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="29322-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

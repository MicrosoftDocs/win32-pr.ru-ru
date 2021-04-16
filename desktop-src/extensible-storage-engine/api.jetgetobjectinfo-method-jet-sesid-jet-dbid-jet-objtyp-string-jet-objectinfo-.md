---
description: 'Дополнительные сведения: метод API. Жетжетобжектинфо (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)'
title: Метод API. Жетжетобжектинфо (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
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
ms.openlocfilehash: 01311dcfbba226405a3c46c1be4c4553eac4eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692214"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a><span data-ttu-id="1da04-103">Метод API. Жетжетобжектинфо (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</span><span class="sxs-lookup"><span data-stu-id="1da04-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</span></span>

<span data-ttu-id="1da04-104">Извлекает сведения об объектах базы данных.</span><span class="sxs-lookup"><span data-stu-id="1da04-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="1da04-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1da04-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1da04-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1da04-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1da04-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1da04-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="1da04-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1da04-108">Parameters</span></span>

  - <span data-ttu-id="1da04-109">сесид</span><span class="sxs-lookup"><span data-stu-id="1da04-109">sesid</span></span>  
    <span data-ttu-id="1da04-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1da04-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1da04-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1da04-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1da04-112">dbid</span><span class="sxs-lookup"><span data-stu-id="1da04-112">dbid</span></span>  
    <span data-ttu-id="1da04-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1da04-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1da04-114">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="1da04-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1da04-115">обжтип</span><span class="sxs-lookup"><span data-stu-id="1da04-115">objtyp</span></span>  
    <span data-ttu-id="1da04-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1da04-116">Type: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="1da04-117">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="1da04-117">The type of the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="1da04-118">ИмяОбъекта</span><span class="sxs-lookup"><span data-stu-id="1da04-118">objectName</span></span>  
    <span data-ttu-id="1da04-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1da04-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1da04-120">Имя объекта, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1da04-120">The object name about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="1da04-121">обжектинфо</span><span class="sxs-lookup"><span data-stu-id="1da04-121">objectinfo</span></span>  
    <span data-ttu-id="1da04-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="1da04-122">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="1da04-123">Заполняется сведениями об объектах в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1da04-123">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="1da04-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1da04-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1da04-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="1da04-125">Reference</span></span>

[<span data-ttu-id="1da04-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="1da04-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1da04-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="1da04-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1da04-128">Перегрузка Жетжетобжектинфо</span><span class="sxs-lookup"><span data-stu-id="1da04-128">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="1da04-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1da04-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

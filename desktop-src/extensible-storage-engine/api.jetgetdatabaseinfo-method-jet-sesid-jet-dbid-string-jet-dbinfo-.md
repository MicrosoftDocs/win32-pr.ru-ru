---
description: 'Дополнительные сведения: метод API. Жетжетдатабасеинфо (JET_SESID, JET_DBID, String, JET_DbInfo)'
title: Метод API. Жетжетдатабасеинфо (JET_SESID, JET_DBID, String, JET_DbInfo)
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100714
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d07ce09ac97a59936a47103067b32f348ed2ff56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673222"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-string-jet_dbinfo"></a><span data-ttu-id="796a5-103">Метод API. Жетжетдатабасеинфо (JET_SESID, JET_DBID, String, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="796a5-103">Api.JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)</span></span>

<span data-ttu-id="796a5-104">Извлекает определенные сведения о заданной базе данных.</span><span class="sxs-lookup"><span data-stu-id="796a5-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="796a5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="796a5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="796a5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="796a5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="796a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="796a5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef value As String, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim value As String
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out string value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="796a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="796a5-108">Parameters</span></span>

  - <span data-ttu-id="796a5-109">сесид</span><span class="sxs-lookup"><span data-stu-id="796a5-109">sesid</span></span>  
    <span data-ttu-id="796a5-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="796a5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="796a5-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="796a5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="796a5-112">dbid</span><span class="sxs-lookup"><span data-stu-id="796a5-112">dbid</span></span>  
    <span data-ttu-id="796a5-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="796a5-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="796a5-114">Идентификатор базы данных.</span><span class="sxs-lookup"><span data-stu-id="796a5-114">The database identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="796a5-115">значение</span><span class="sxs-lookup"><span data-stu-id="796a5-115">value</span></span>  
    <span data-ttu-id="796a5-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="796a5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="796a5-117">Получаемое значение.</span><span class="sxs-lookup"><span data-stu-id="796a5-117">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="796a5-118">инфолевел</span><span class="sxs-lookup"><span data-stu-id="796a5-118">infoLevel</span></span>  
    <span data-ttu-id="796a5-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="796a5-119">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="796a5-120">Конкретные извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="796a5-120">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="796a5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="796a5-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="796a5-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="796a5-122">Reference</span></span>

[<span data-ttu-id="796a5-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="796a5-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="796a5-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="796a5-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="796a5-125">Перегрузка Жетжетдатабасеинфо</span><span class="sxs-lookup"><span data-stu-id="796a5-125">JetGetDatabaseInfo overload</span></span>](./api.jetgetdatabaseinfo-method.md)

[<span data-ttu-id="796a5-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="796a5-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: Дополнительные сведения о методе API. Жеткреатедатабасе
title: API. Жеткреатедатабасе, метод
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673227"
---
# <a name="apijetcreatedatabase-method"></a><span data-ttu-id="705fd-103">API. Жеткреатедатабасе, метод</span><span class="sxs-lookup"><span data-stu-id="705fd-103">Api.JetCreateDatabase method</span></span>

<span data-ttu-id="705fd-104">Создает и прикрепляет файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="705fd-104">Creates and attaches a database file.</span></span>

<span data-ttu-id="705fd-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="705fd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="705fd-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="705fd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="705fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="705fd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="705fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="705fd-108">Parameters</span></span>

  - <span data-ttu-id="705fd-109">сесид</span><span class="sxs-lookup"><span data-stu-id="705fd-109">sesid</span></span>  
    <span data-ttu-id="705fd-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="705fd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="705fd-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="705fd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="705fd-112">База данных</span><span class="sxs-lookup"><span data-stu-id="705fd-112">database</span></span>  
    <span data-ttu-id="705fd-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="705fd-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="705fd-114">Путь к создаваемому файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="705fd-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="705fd-115">подключение</span><span class="sxs-lookup"><span data-stu-id="705fd-115">connect</span></span>  
    <span data-ttu-id="705fd-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="705fd-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="705fd-117">Параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="705fd-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="705fd-118">dbid</span><span class="sxs-lookup"><span data-stu-id="705fd-118">dbid</span></span>  
    <span data-ttu-id="705fd-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="705fd-119">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="705fd-120">Возвращает DBID новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="705fd-120">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="705fd-121">грбит</span><span class="sxs-lookup"><span data-stu-id="705fd-121">grbit</span></span>  
    <span data-ttu-id="705fd-122">Тип: [Microsoft. ISAM. ESENT. Interop. креатедатабасегрбит](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="705fd-122">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="705fd-123">Параметры создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="705fd-123">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="705fd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="705fd-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="705fd-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="705fd-125">Reference</span></span>

[<span data-ttu-id="705fd-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="705fd-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="705fd-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="705fd-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="705fd-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="705fd-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: Дополнительные сведения о методе API. JetCreateDatabase2
title: API. JetCreateDatabase2, метод
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808273"
---
# <a name="apijetcreatedatabase2-method"></a><span data-ttu-id="598dd-103">API. JetCreateDatabase2, метод</span><span class="sxs-lookup"><span data-stu-id="598dd-103">Api.JetCreateDatabase2 method</span></span>

<span data-ttu-id="598dd-104">Создает и прикрепляет файл базы данных с указанным максимальным размером базы данных.</span><span class="sxs-lookup"><span data-stu-id="598dd-104">Creates and attaches a database file with a maximum database size specified.</span></span>

<span data-ttu-id="598dd-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="598dd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="598dd-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="598dd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="598dd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="598dd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="598dd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="598dd-108">Parameters</span></span>

  - <span data-ttu-id="598dd-109">сесид</span><span class="sxs-lookup"><span data-stu-id="598dd-109">sesid</span></span>  
    <span data-ttu-id="598dd-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="598dd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="598dd-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="598dd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="598dd-112">База данных</span><span class="sxs-lookup"><span data-stu-id="598dd-112">database</span></span>  
    <span data-ttu-id="598dd-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="598dd-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="598dd-114">Путь к создаваемому файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="598dd-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="598dd-115">макспажес</span><span class="sxs-lookup"><span data-stu-id="598dd-115">maxPages</span></span>  
    <span data-ttu-id="598dd-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="598dd-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="598dd-117">Максимальный размер базы данных в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="598dd-117">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="598dd-118">Передача значения 0 означает отсутствие принудительного применения максимального значения.</span><span class="sxs-lookup"><span data-stu-id="598dd-118">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="598dd-119">dbid</span><span class="sxs-lookup"><span data-stu-id="598dd-119">dbid</span></span>  
    <span data-ttu-id="598dd-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="598dd-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="598dd-121">Возвращает DBID новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="598dd-121">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="598dd-122">грбит</span><span class="sxs-lookup"><span data-stu-id="598dd-122">grbit</span></span>  
    <span data-ttu-id="598dd-123">Тип: [Microsoft. ISAM. ESENT. Interop. креатедатабасегрбит](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="598dd-123">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="598dd-124">Параметры создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="598dd-124">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="598dd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="598dd-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="598dd-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="598dd-126">Reference</span></span>

[<span data-ttu-id="598dd-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="598dd-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="598dd-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="598dd-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="598dd-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="598dd-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

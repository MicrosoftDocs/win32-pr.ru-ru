---
description: Дополнительные сведения о методе API. Жетопендатабасе
title: API. Жетопендатабасе, метод
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272549"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="d2922-103">API. Жетопендатабасе, метод</span><span class="sxs-lookup"><span data-stu-id="d2922-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="d2922-104">Открывает базу данных, ранее присоединенную с помощью [жетаттачдатабасе (JET_SESID, String, аттачдатабасегрбит)](./api.jetattachdatabase-method.md), для использования с сеансом базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2922-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="d2922-105">Эту функцию можно вызывать несколько раз для одной и той же базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2922-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="d2922-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2922-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2922-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2922-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2922-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2922-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d2922-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2922-109">Parameters</span></span>

  - <span data-ttu-id="d2922-110">сесид</span><span class="sxs-lookup"><span data-stu-id="d2922-110">sesid</span></span>  
    <span data-ttu-id="d2922-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2922-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d2922-112">Сеанс, в котором открывается база данных.</span><span class="sxs-lookup"><span data-stu-id="d2922-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2922-113">База данных</span><span class="sxs-lookup"><span data-stu-id="d2922-113">database</span></span>  
    <span data-ttu-id="d2922-114">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d2922-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d2922-115">Открываемая база данных.</span><span class="sxs-lookup"><span data-stu-id="d2922-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2922-116">подключение</span><span class="sxs-lookup"><span data-stu-id="d2922-116">connect</span></span>  
    <span data-ttu-id="d2922-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d2922-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d2922-118">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="d2922-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2922-119">dbid</span><span class="sxs-lookup"><span data-stu-id="d2922-119">dbid</span></span>  
    <span data-ttu-id="d2922-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2922-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d2922-121">Возвращает DBID присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2922-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2922-122">грбит</span><span class="sxs-lookup"><span data-stu-id="d2922-122">grbit</span></span>  
    <span data-ttu-id="d2922-123">Тип: [Microsoft. ISAM. ESENT. Interop. опендатабасегрбит](./opendatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d2922-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d2922-124">Откройте параметры базы данных.</span><span class="sxs-lookup"><span data-stu-id="d2922-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d2922-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2922-125">Return value</span></span>

<span data-ttu-id="d2922-126">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d2922-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="d2922-127">Код предупреждения ESENT.</span><span class="sxs-lookup"><span data-stu-id="d2922-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2922-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2922-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2922-129">Справочник</span><span class="sxs-lookup"><span data-stu-id="d2922-129">Reference</span></span>

[<span data-ttu-id="d2922-130">Класс API</span><span class="sxs-lookup"><span data-stu-id="d2922-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d2922-131">Члены API</span><span class="sxs-lookup"><span data-stu-id="d2922-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d2922-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d2922-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

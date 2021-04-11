---
description: Дополнительные сведения о методе API. JetDetachDatabase2
title: API. JetDetachDatabase2, метод
TOCTitle: 'JetDetachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55100685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44cc8b5d03ba720f1acb7d0e8603bf29906a611e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144344"
---
# <a name="apijetdetachdatabase2-method"></a><span data-ttu-id="44e32-103">API. JetDetachDatabase2, метод</span><span class="sxs-lookup"><span data-stu-id="44e32-103">Api.JetDetachDatabase2 method</span></span>

<span data-ttu-id="44e32-104">Освобождает файл базы данных, который был ранее присоединен к сеансу базы данных.</span><span class="sxs-lookup"><span data-stu-id="44e32-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="44e32-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44e32-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44e32-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44e32-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44e32-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44e32-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As DetachDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As DetachDatabaseGrbitApi.JetDetachDatabase2(sesid, database, _
    grbit)
```

``` csharp
public static void JetDetachDatabase2(
    JET_SESID sesid,
    string database,
    DetachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="44e32-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44e32-108">Parameters</span></span>

  - <span data-ttu-id="44e32-109">сесид</span><span class="sxs-lookup"><span data-stu-id="44e32-109">sesid</span></span>  
    <span data-ttu-id="44e32-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44e32-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="44e32-111">Используемый сеанс базы данных.</span><span class="sxs-lookup"><span data-stu-id="44e32-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="44e32-112">База данных</span><span class="sxs-lookup"><span data-stu-id="44e32-112">database</span></span>  
    <span data-ttu-id="44e32-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="44e32-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="44e32-114">База данных для отсоединения.</span><span class="sxs-lookup"><span data-stu-id="44e32-114">The database to detach.</span></span>

<!-- end list -->

  - <span data-ttu-id="44e32-115">грбит</span><span class="sxs-lookup"><span data-stu-id="44e32-115">grbit</span></span>  
    <span data-ttu-id="44e32-116">Тип: [Microsoft. ISAM. ESENT. Interop. детачдатабасегрбит](./detachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="44e32-116">Type: [Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit](./detachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="44e32-117">Параметры отсоединения.</span><span class="sxs-lookup"><span data-stu-id="44e32-117">Detach options.</span></span>

## <a name="see-also"></a><span data-ttu-id="44e32-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44e32-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44e32-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="44e32-119">Reference</span></span>

[<span data-ttu-id="44e32-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="44e32-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="44e32-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="44e32-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="44e32-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="44e32-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

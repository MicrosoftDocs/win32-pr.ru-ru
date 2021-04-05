---
description: Дополнительные сведения о методе API. Жетгровдатабасе
title: API. Жетгровдатабасе, метод
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a51f0d55187b6f6eac66c0cba2ec7b9daa7d1dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897993"
---
# <a name="apijetgrowdatabase-method"></a><span data-ttu-id="9adad-103">API. Жетгровдатабасе, метод</span><span class="sxs-lookup"><span data-stu-id="9adad-103">Api.JetGrowDatabase method</span></span>

<span data-ttu-id="9adad-104">Увеличивает размер открытой в данный момент базы данных.</span><span class="sxs-lookup"><span data-stu-id="9adad-104">Extends the size of a database that is currently open.</span></span>

<span data-ttu-id="9adad-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9adad-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9adad-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9adad-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9adad-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9adad-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="9adad-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9adad-108">Parameters</span></span>

  - <span data-ttu-id="9adad-109">сесид</span><span class="sxs-lookup"><span data-stu-id="9adad-109">sesid</span></span>  
    <span data-ttu-id="9adad-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9adad-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9adad-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="9adad-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9adad-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9adad-112">dbid</span></span>  
    <span data-ttu-id="9adad-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9adad-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9adad-114">База данных для увеличения.</span><span class="sxs-lookup"><span data-stu-id="9adad-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="9adad-115">десиредпажес</span><span class="sxs-lookup"><span data-stu-id="9adad-115">desiredPages</span></span>  
    <span data-ttu-id="9adad-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9adad-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9adad-117">Требуемый размер базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="9adad-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="9adad-118">актуалпажес</span><span class="sxs-lookup"><span data-stu-id="9adad-118">actualPages</span></span>  
    <span data-ttu-id="9adad-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9adad-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9adad-120">Размер базы данных на страницах после вызова.</span><span class="sxs-lookup"><span data-stu-id="9adad-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="9adad-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9adad-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9adad-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="9adad-122">Reference</span></span>

[<span data-ttu-id="9adad-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="9adad-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9adad-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="9adad-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9adad-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9adad-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: Дополнительные сведения о методе API. Жеткомпутестатс
title: API. Жеткомпутестатс, метод
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262839"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="28e17-103">API. Жеткомпутестатс, метод</span><span class="sxs-lookup"><span data-stu-id="28e17-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="28e17-104">Просматривает каждый индекс таблицы, чтобы точно вычислить количество записей в индексе и количество различных ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="28e17-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="28e17-105">Эти сведения вместе с количеством страниц базы данных, выделенных для индекса, и текущим временем вычислений хранятся в метаданных индекса в базе данных.</span><span class="sxs-lookup"><span data-stu-id="28e17-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="28e17-106">Эти данные можно впоследствии извлечь с помощью информационных операций.</span><span class="sxs-lookup"><span data-stu-id="28e17-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="28e17-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28e17-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28e17-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="28e17-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28e17-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28e17-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="28e17-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="28e17-110">Parameters</span></span>

  - <span data-ttu-id="28e17-111">сесид</span><span class="sxs-lookup"><span data-stu-id="28e17-111">sesid</span></span>  
    <span data-ttu-id="28e17-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="28e17-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="28e17-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="28e17-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="28e17-114">TableID</span><span class="sxs-lookup"><span data-stu-id="28e17-114">tableid</span></span>  
    <span data-ttu-id="28e17-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="28e17-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="28e17-116">Таблица, для которой будет вычисляться статистика.</span><span class="sxs-lookup"><span data-stu-id="28e17-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="28e17-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28e17-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28e17-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="28e17-118">Reference</span></span>

[<span data-ttu-id="28e17-119">Класс API</span><span class="sxs-lookup"><span data-stu-id="28e17-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="28e17-120">Члены API</span><span class="sxs-lookup"><span data-stu-id="28e17-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="28e17-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="28e17-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения о методе: Windows8Api. JetCreateIndex4'
title: Windows8Api. JetCreateIndex4, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155219"
---
# <a name="windows8apijetcreateindex4-method"></a><span data-ttu-id="5e9ae-103">Windows8Api. JetCreateIndex4, метод</span><span class="sxs-lookup"><span data-stu-id="5e9ae-103">Windows8Api.JetCreateIndex4 method</span></span>

<span data-ttu-id="5e9ae-104">Создает индексы для данных в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="5e9ae-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="5e9ae-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e9ae-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="5e9ae-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e9ae-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e9ae-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="5e9ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e9ae-108">Parameters</span></span>

  - <span data-ttu-id="5e9ae-109">сесид</span><span class="sxs-lookup"><span data-stu-id="5e9ae-109">sesid</span></span>  
    <span data-ttu-id="5e9ae-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5e9ae-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5e9ae-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="5e9ae-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e9ae-112">TableID</span><span class="sxs-lookup"><span data-stu-id="5e9ae-112">tableid</span></span>  
    <span data-ttu-id="5e9ae-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5e9ae-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5e9ae-114">Таблица, в которой создается индекс.</span><span class="sxs-lookup"><span data-stu-id="5e9ae-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e9ae-115">индекскреатес</span><span class="sxs-lookup"><span data-stu-id="5e9ae-115">indexcreates</span></span>  
    <span data-ttu-id="5e9ae-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="5e9ae-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="5e9ae-117">Массив объектов, описывающих создаваемые индексы.</span><span class="sxs-lookup"><span data-stu-id="5e9ae-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e9ae-118">нуминдекскреатес</span><span class="sxs-lookup"><span data-stu-id="5e9ae-118">numIndexCreates</span></span>  
    <span data-ttu-id="5e9ae-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5e9ae-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5e9ae-120">Число объектов описания индекса.</span><span class="sxs-lookup"><span data-stu-id="5e9ae-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9ae-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e9ae-121">Remarks</span></span>

<span data-ttu-id="5e9ae-122">При создании нескольких индексов (т. е. с Нуминдекскреатес больше 1) Этот метод должен вызываться за пределами транзакций и с монопольным доступом к таблице.</span><span class="sxs-lookup"><span data-stu-id="5e9ae-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="5e9ae-123">JET_TABLEID, возвращаемый "API. Жеткреатетабле", будет иметь доступ только, или таблицу можно открыть для монопольного доступа, передав [дениреад](./opentablegrbit-enumeration.md) в [жетопентабле (JET_SESID, JET_DBID, String, \[ \] , Int32, опентаблегрбит, JET_TABLEID)](./api.jetopentable-method.md).</span><span class="sxs-lookup"><span data-stu-id="5e9ae-123">The JET_TABLEID returned by "Api.JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5e9ae-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e9ae-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e9ae-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="5e9ae-125">Reference</span></span>

[<span data-ttu-id="5e9ae-126">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5e9ae-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="5e9ae-127">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5e9ae-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="5e9ae-128">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="5e9ae-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

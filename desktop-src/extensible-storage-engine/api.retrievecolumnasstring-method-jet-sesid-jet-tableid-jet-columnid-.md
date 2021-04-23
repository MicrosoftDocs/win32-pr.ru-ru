---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100860
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64500e9827d55fab4771963b95dbfd0efffdc5c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693541"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="06e94-103">Метод API. Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="06e94-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="06e94-104">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="06e94-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="06e94-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="06e94-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="06e94-106">Используется кодировка Юникод.</span><span class="sxs-lookup"><span data-stu-id="06e94-106">The Unicode encoding is used.</span></span>

<span data-ttu-id="06e94-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06e94-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06e94-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="06e94-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06e94-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06e94-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="06e94-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="06e94-110">Parameters</span></span>

  - <span data-ttu-id="06e94-111">сесид</span><span class="sxs-lookup"><span data-stu-id="06e94-111">sesid</span></span>  
    <span data-ttu-id="06e94-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06e94-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="06e94-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="06e94-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="06e94-114">TableID</span><span class="sxs-lookup"><span data-stu-id="06e94-114">tableid</span></span>  
    <span data-ttu-id="06e94-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06e94-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="06e94-116">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="06e94-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="06e94-117">columnid</span><span class="sxs-lookup"><span data-stu-id="06e94-117">columnid</span></span>  
    <span data-ttu-id="06e94-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06e94-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="06e94-119">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="06e94-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="06e94-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06e94-120">Return value</span></span>

<span data-ttu-id="06e94-121">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="06e94-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="06e94-122">Данные, полученные из столбца в виде строки.</span><span class="sxs-lookup"><span data-stu-id="06e94-122">The data retrieved from the column as a string.</span></span> <span data-ttu-id="06e94-123">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="06e94-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="06e94-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06e94-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06e94-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="06e94-125">Reference</span></span>

[<span data-ttu-id="06e94-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="06e94-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="06e94-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="06e94-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="06e94-128">Перегрузка Ретриевеколумнасстринг</span><span class="sxs-lookup"><span data-stu-id="06e94-128">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="06e94-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="06e94-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

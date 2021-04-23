---
description: 'Дополнительные сведения: метод API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100894
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2e6bb69ca1b278cbb930de7c20611645283ee59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693543"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="b2caf-103">Метод API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="b2caf-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="b2caf-104">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b2caf-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b2caf-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="b2caf-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="b2caf-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2caf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b2caf-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2caf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2caf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2caf-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="b2caf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2caf-109">Parameters</span></span>

  - <span data-ttu-id="b2caf-110">сесид</span><span class="sxs-lookup"><span data-stu-id="b2caf-110">sesid</span></span>  
    <span data-ttu-id="b2caf-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2caf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b2caf-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="b2caf-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2caf-113">TableID</span><span class="sxs-lookup"><span data-stu-id="b2caf-113">tableid</span></span>  
    <span data-ttu-id="b2caf-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2caf-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b2caf-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="b2caf-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2caf-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b2caf-116">columnid</span></span>  
    <span data-ttu-id="b2caf-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2caf-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b2caf-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="b2caf-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b2caf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2caf-119">Return value</span></span>

<span data-ttu-id="b2caf-120">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="b2caf-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="b2caf-121">Данные, полученные из столбца в виде целого числа. Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b2caf-121">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2caf-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2caf-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2caf-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="b2caf-123">Reference</span></span>

[<span data-ttu-id="b2caf-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="b2caf-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b2caf-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="b2caf-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b2caf-126">Перегрузка RetrieveColumnAsInt32</span><span class="sxs-lookup"><span data-stu-id="b2caf-126">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="b2caf-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b2caf-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения: метод API. Жеттаблеиндексес (JET_SESID, JET_TABLEID)'
title: Метод API. Жеттаблеиндексес (JET_SESID, JET_TABLEID)
TOCTitle: GetTableIndexes method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55107219
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8708f285445b13ecb1c9d2cb306ec14c7976905b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701428"
---
# <a name="apigettableindexes-method-jet_sesid-jet_tableid"></a><span data-ttu-id="616e0-103">Метод API. Жеттаблеиндексес (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="616e0-103">Api.GetTableIndexes method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="616e0-104">Выполняет перебор всех индексов в таблице, возвращая сведения о каждой из них.</span><span class="sxs-lookup"><span data-stu-id="616e0-104">Iterates over all the indexes in the table, returning information about each one.</span></span>

<span data-ttu-id="616e0-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="616e0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="616e0-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="616e0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="616e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="616e0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="616e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="616e0-108">Parameters</span></span>

  - <span data-ttu-id="616e0-109">сесид</span><span class="sxs-lookup"><span data-stu-id="616e0-109">sesid</span></span>  
    <span data-ttu-id="616e0-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="616e0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="616e0-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="616e0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="616e0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="616e0-112">tableid</span></span>  
    <span data-ttu-id="616e0-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="616e0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="616e0-114">Таблица, для которой необходимо получить сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="616e0-114">The table to retrieve index information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="616e0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="616e0-115">Return value</span></span>

<span data-ttu-id="616e0-116">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="616e0-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="616e0-117">Итератор по Индексинфо для каждого индекса в таблице.</span><span class="sxs-lookup"><span data-stu-id="616e0-117">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="616e0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="616e0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="616e0-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="616e0-119">Reference</span></span>

[<span data-ttu-id="616e0-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="616e0-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="616e0-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="616e0-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="616e0-122">Перегрузка Жеттаблеиндексес</span><span class="sxs-lookup"><span data-stu-id="616e0-122">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="616e0-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="616e0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Дополнительные сведения: метод API. Жеттаблеколумнс (JET_SESID, JET_TABLEID)'
title: Метод API. Жеттаблеколумнс (JET_SESID, JET_TABLEID)
TOCTitle: GetTableColumns method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107218
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 393f730920ce7abb3ef24916c9e1c9e9591ba020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143381"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_tableid"></a><span data-ttu-id="a475f-103">Метод API. Жеттаблеколумнс (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="a475f-103">Api.GetTableColumns method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="a475f-104">Выполняет перебор всех столбцов в таблице, возвращая сведения о каждом из них.</span><span class="sxs-lookup"><span data-stu-id="a475f-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="a475f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a475f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a475f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a475f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a475f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a475f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="a475f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a475f-108">Parameters</span></span>

  - <span data-ttu-id="a475f-109">сесид</span><span class="sxs-lookup"><span data-stu-id="a475f-109">sesid</span></span>  
    <span data-ttu-id="a475f-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a475f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a475f-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a475f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a475f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a475f-112">tableid</span></span>  
    <span data-ttu-id="a475f-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a475f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a475f-114">Таблица, для которой необходимо получить сведения о столбцах.</span><span class="sxs-lookup"><span data-stu-id="a475f-114">The table to retrieve column information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a475f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a475f-115">Return value</span></span>

<span data-ttu-id="a475f-116">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="a475f-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="a475f-117">Итератор по ColumnInfo для каждого столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="a475f-117">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a475f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a475f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a475f-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="a475f-119">Reference</span></span>

[<span data-ttu-id="a475f-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="a475f-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a475f-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="a475f-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a475f-122">Перегрузка Жеттаблеколумнс</span><span class="sxs-lookup"><span data-stu-id="a475f-122">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="a475f-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a475f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

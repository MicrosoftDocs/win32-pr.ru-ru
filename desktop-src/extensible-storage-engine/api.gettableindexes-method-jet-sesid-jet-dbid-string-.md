---
description: 'Дополнительные сведения: метод API. Жеттаблеиндексес (JET_SESID, JET_DBID, String)'
title: Метод API. Жеттаблеиндексес (JET_SESID, JET_DBID, String)
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
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
ms.openlocfilehash: 90ac8dd014e0594fbffbb12b3ea4f3698f850de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896610"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="d4bff-103">Метод API. Жеттаблеиндексес (JET_SESID, JET_DBID, String)</span><span class="sxs-lookup"><span data-stu-id="d4bff-103">Api.GetTableIndexes method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="d4bff-104">Выполняет перебор всех индексов в таблице, возвращая сведения о каждой из них.</span><span class="sxs-lookup"><span data-stu-id="d4bff-104">Iterates over all the indexs in the table, returning information about each one.</span></span>

<span data-ttu-id="d4bff-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d4bff-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d4bff-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d4bff-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d4bff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4bff-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="d4bff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4bff-108">Parameters</span></span>

  - <span data-ttu-id="d4bff-109">сесид</span><span class="sxs-lookup"><span data-stu-id="d4bff-109">sesid</span></span>  
    <span data-ttu-id="d4bff-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4bff-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d4bff-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d4bff-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4bff-112">dbid</span><span class="sxs-lookup"><span data-stu-id="d4bff-112">dbid</span></span>  
    <span data-ttu-id="d4bff-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4bff-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d4bff-114">База данных, содержащая таблицу.</span><span class="sxs-lookup"><span data-stu-id="d4bff-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4bff-115">tablename</span><span class="sxs-lookup"><span data-stu-id="d4bff-115">tablename</span></span>  
    <span data-ttu-id="d4bff-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d4bff-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d4bff-117">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4bff-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d4bff-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4bff-118">Return value</span></span>

<span data-ttu-id="d4bff-119">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="d4bff-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="d4bff-120">Итератор по Индексинфо для каждого индекса в таблице.</span><span class="sxs-lookup"><span data-stu-id="d4bff-120">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d4bff-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4bff-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d4bff-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="d4bff-122">Reference</span></span>

[<span data-ttu-id="d4bff-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="d4bff-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d4bff-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="d4bff-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d4bff-125">Перегрузка Жеттаблеиндексес</span><span class="sxs-lookup"><span data-stu-id="d4bff-125">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="d4bff-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d4bff-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

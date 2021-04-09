---
description: Дополнительные сведения см. в описании метода API.-TableNames.
title: API. методы. TableName
TOCTitle: 'GetTableNames method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableNames(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablenames(v=EXCHG.10)
ms:contentKeyID: 55100650
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39a52d62ae5271353350df15c4c00833266094cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144365"
---
# <a name="apigettablenames-method"></a><span data-ttu-id="9bdcd-103">API. методы. TableName</span><span class="sxs-lookup"><span data-stu-id="9bdcd-103">Api.GetTableNames method</span></span>

<span data-ttu-id="9bdcd-104">Возвращает имена таблиц в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-104">Returns the names of the tables in the database.</span></span>

<span data-ttu-id="9bdcd-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bdcd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9bdcd-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bdcd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bdcd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bdcd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableNames ( _
    sesid As JET_SESID, _
    dbid As JET_DBID _
) As IEnumerable(Of String)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim returnValue As IEnumerable(Of String)

returnValue = Api.GetTableNames(sesid, _
    dbid)
```

``` csharp
public static IEnumerable<string> GetTableNames(
    JET_SESID sesid,
    JET_DBID dbid
)
```

#### <a name="parameters"></a><span data-ttu-id="9bdcd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bdcd-108">Parameters</span></span>

  - <span data-ttu-id="9bdcd-109">сесид</span><span class="sxs-lookup"><span data-stu-id="9bdcd-109">sesid</span></span>  
    <span data-ttu-id="9bdcd-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bdcd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9bdcd-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bdcd-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9bdcd-112">dbid</span></span>  
    <span data-ttu-id="9bdcd-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bdcd-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9bdcd-114">База данных, содержащая таблицу.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-114">The database containing the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9bdcd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bdcd-115">Return value</span></span>

<span data-ttu-id="9bdcd-116">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="9bdcd-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span></span>  
<span data-ttu-id="9bdcd-117">Итератор по именам таблиц в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9bdcd-117">An iterator over the names of the tables in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bdcd-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bdcd-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bdcd-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="9bdcd-119">Reference</span></span>

[<span data-ttu-id="9bdcd-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="9bdcd-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9bdcd-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="9bdcd-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9bdcd-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9bdcd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

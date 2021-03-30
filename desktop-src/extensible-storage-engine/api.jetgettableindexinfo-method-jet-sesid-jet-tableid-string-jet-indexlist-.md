---
description: 'Дополнительные сведения: метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)'
title: Метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a39fba54463f7a55fd6a8521f5c905da4afb4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263415"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a><span data-ttu-id="c1d51-103">Метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="c1d51-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="c1d51-104">**Примечание. Теперь этот API устарел.**</span><span class="sxs-lookup"><span data-stu-id="c1d51-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="c1d51-105">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="c1d51-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="c1d51-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1d51-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1d51-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c1d51-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d51-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1d51-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="c1d51-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1d51-109">Parameters</span></span>

  - <span data-ttu-id="c1d51-110">сесид</span><span class="sxs-lookup"><span data-stu-id="c1d51-110">sesid</span></span>  
    <span data-ttu-id="c1d51-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1d51-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c1d51-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c1d51-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1d51-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c1d51-113">tableid</span></span>  
    <span data-ttu-id="c1d51-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1d51-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c1d51-115">Таблица для получения сведений об индексе.</span><span class="sxs-lookup"><span data-stu-id="c1d51-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1d51-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="c1d51-116">indexname</span></span>  
    <span data-ttu-id="c1d51-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c1d51-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c1d51-118">Этот параметр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="c1d51-118">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1d51-119">индекслист</span><span class="sxs-lookup"><span data-stu-id="c1d51-119">indexlist</span></span>  
    <span data-ttu-id="c1d51-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="c1d51-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="c1d51-121">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="c1d51-121">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1d51-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1d51-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1d51-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="c1d51-123">Reference</span></span>

[<span data-ttu-id="c1d51-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="c1d51-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c1d51-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="c1d51-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c1d51-126">Перегрузка Жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="c1d51-126">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="c1d51-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c1d51-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

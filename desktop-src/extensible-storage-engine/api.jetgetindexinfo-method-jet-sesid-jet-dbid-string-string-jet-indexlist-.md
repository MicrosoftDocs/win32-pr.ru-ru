---
description: 'Дополнительные сведения: метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST)'
title: Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673219"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a><span data-ttu-id="24482-103">Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="24482-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="24482-104">**Примечание. Теперь этот API устарел.**</span><span class="sxs-lookup"><span data-stu-id="24482-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="24482-105">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="24482-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="24482-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24482-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24482-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24482-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24482-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24482-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="24482-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="24482-109">Parameters</span></span>

  - <span data-ttu-id="24482-110">сесид</span><span class="sxs-lookup"><span data-stu-id="24482-110">sesid</span></span>  
    <span data-ttu-id="24482-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24482-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="24482-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="24482-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="24482-113">dbid</span><span class="sxs-lookup"><span data-stu-id="24482-113">dbid</span></span>  
    <span data-ttu-id="24482-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24482-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="24482-115">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="24482-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="24482-116">tablename</span><span class="sxs-lookup"><span data-stu-id="24482-116">tablename</span></span>  
    <span data-ttu-id="24482-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="24482-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="24482-118">Имя таблицы, о которой необходимо получить сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="24482-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="24482-119">не учитывается</span><span class="sxs-lookup"><span data-stu-id="24482-119">ignored</span></span>  
    <span data-ttu-id="24482-120">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="24482-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="24482-121">Этот параметр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="24482-121">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="24482-122">индекслист</span><span class="sxs-lookup"><span data-stu-id="24482-122">indexlist</span></span>  
    <span data-ttu-id="24482-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="24482-123">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="24482-124">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="24482-124">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="24482-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24482-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24482-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="24482-126">Reference</span></span>

[<span data-ttu-id="24482-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="24482-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="24482-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="24482-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="24482-129">Перегрузка Жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="24482-129">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="24482-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="24482-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

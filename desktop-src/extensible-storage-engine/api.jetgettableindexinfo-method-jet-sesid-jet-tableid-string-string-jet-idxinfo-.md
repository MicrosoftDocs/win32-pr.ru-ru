---
description: 'Дополнительные сведения: метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, строка, JET_IdxInfo)'
title: Метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, строка, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100750
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62291587ca1c07da74c2b646870751f3b8af981b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711339"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-string-jet_idxinfo"></a><span data-ttu-id="08d57-103">Метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, строка, строка, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="08d57-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="08d57-104">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="08d57-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="08d57-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08d57-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08d57-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08d57-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08d57-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08d57-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="08d57-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08d57-108">Parameters</span></span>

  - <span data-ttu-id="08d57-109">сесид</span><span class="sxs-lookup"><span data-stu-id="08d57-109">sesid</span></span>  
    <span data-ttu-id="08d57-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="08d57-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="08d57-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="08d57-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="08d57-112">TableID</span><span class="sxs-lookup"><span data-stu-id="08d57-112">tableid</span></span>  
    <span data-ttu-id="08d57-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="08d57-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="08d57-114">Таблица для получения сведений об индексе.</span><span class="sxs-lookup"><span data-stu-id="08d57-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="08d57-115">IndexName</span><span class="sxs-lookup"><span data-stu-id="08d57-115">indexname</span></span>  
    <span data-ttu-id="08d57-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="08d57-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="08d57-117">Имя индекса.</span><span class="sxs-lookup"><span data-stu-id="08d57-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="08d57-118">result</span><span class="sxs-lookup"><span data-stu-id="08d57-118">result</span></span>  
    <span data-ttu-id="08d57-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="08d57-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="08d57-120">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="08d57-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="08d57-121">инфолевел</span><span class="sxs-lookup"><span data-stu-id="08d57-121">infoLevel</span></span>  
    <span data-ttu-id="08d57-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="08d57-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="08d57-123">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="08d57-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="08d57-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08d57-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08d57-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="08d57-125">Reference</span></span>

[<span data-ttu-id="08d57-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="08d57-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="08d57-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="08d57-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="08d57-128">Перегрузка Жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="08d57-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="08d57-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="08d57-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

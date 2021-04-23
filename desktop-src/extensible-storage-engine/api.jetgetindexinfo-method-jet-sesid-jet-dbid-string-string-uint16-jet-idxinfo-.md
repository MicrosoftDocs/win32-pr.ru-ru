---
description: 'Дополнительные сведения: метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)'
title: Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, UInt16, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 762437dba9e502de5c0650e4ae6df53d4629d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650504"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a><span data-ttu-id="12fde-103">Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="12fde-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="12fde-104">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="12fde-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="12fde-105">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="12fde-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="12fde-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="12fde-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="12fde-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="12fde-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="12fde-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12fde-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="12fde-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="12fde-109">Parameters</span></span>

  - <span data-ttu-id="12fde-110">сесид</span><span class="sxs-lookup"><span data-stu-id="12fde-110">sesid</span></span>  
    <span data-ttu-id="12fde-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="12fde-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="12fde-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="12fde-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="12fde-113">dbid</span><span class="sxs-lookup"><span data-stu-id="12fde-113">dbid</span></span>  
    <span data-ttu-id="12fde-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="12fde-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="12fde-115">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="12fde-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="12fde-116">tablename</span><span class="sxs-lookup"><span data-stu-id="12fde-116">tablename</span></span>  
    <span data-ttu-id="12fde-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="12fde-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="12fde-118">Имя таблицы, о которой необходимо получить сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="12fde-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="12fde-119">IndexName</span><span class="sxs-lookup"><span data-stu-id="12fde-119">indexname</span></span>  
    <span data-ttu-id="12fde-120">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="12fde-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="12fde-121">Имя индекса, сведения о котором необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="12fde-121">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="12fde-122">result</span><span class="sxs-lookup"><span data-stu-id="12fde-122">result</span></span>  
    <span data-ttu-id="12fde-123">Тип: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="12fde-123">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="12fde-124">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="12fde-124">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="12fde-125">инфолевел</span><span class="sxs-lookup"><span data-stu-id="12fde-125">infoLevel</span></span>  
    <span data-ttu-id="12fde-126">Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="12fde-126">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="12fde-127">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="12fde-127">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="12fde-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12fde-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="12fde-129">Справочник</span><span class="sxs-lookup"><span data-stu-id="12fde-129">Reference</span></span>

[<span data-ttu-id="12fde-130">Класс API</span><span class="sxs-lookup"><span data-stu-id="12fde-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="12fde-131">Члены API</span><span class="sxs-lookup"><span data-stu-id="12fde-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="12fde-132">Перегрузка Жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="12fde-132">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="12fde-133">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="12fde-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

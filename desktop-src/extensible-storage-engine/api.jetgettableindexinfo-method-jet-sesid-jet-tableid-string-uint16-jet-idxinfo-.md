---
description: 'Дополнительные сведения: метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)'
title: Метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100747
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
ms.openlocfilehash: 5a5e1f5e6908f33d211c5a32a3b9d34e55098101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712664"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-uint16-jet_idxinfo"></a><span data-ttu-id="4a089-103">Метод API. Жетжеттаблеиндексинфо (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="4a089-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="4a089-104">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="4a089-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="4a089-105">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="4a089-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="4a089-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a089-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a089-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a089-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a089-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a089-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="4a089-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a089-109">Parameters</span></span>

  - <span data-ttu-id="4a089-110">сесид</span><span class="sxs-lookup"><span data-stu-id="4a089-110">sesid</span></span>  
    <span data-ttu-id="4a089-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a089-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4a089-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4a089-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a089-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4a089-113">tableid</span></span>  
    <span data-ttu-id="4a089-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a089-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4a089-115">Таблица для получения сведений об индексе.</span><span class="sxs-lookup"><span data-stu-id="4a089-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a089-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="4a089-116">indexname</span></span>  
    <span data-ttu-id="4a089-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4a089-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4a089-118">Имя индекса.</span><span class="sxs-lookup"><span data-stu-id="4a089-118">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a089-119">result</span><span class="sxs-lookup"><span data-stu-id="4a089-119">result</span></span>  
    <span data-ttu-id="4a089-120">Тип: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="4a089-120">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="4a089-121">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="4a089-121">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a089-122">инфолевел</span><span class="sxs-lookup"><span data-stu-id="4a089-122">infoLevel</span></span>  
    <span data-ttu-id="4a089-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4a089-123">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="4a089-124">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="4a089-124">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a089-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a089-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a089-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="4a089-126">Reference</span></span>

[<span data-ttu-id="4a089-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="4a089-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4a089-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="4a089-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4a089-129">Перегрузка Жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="4a089-129">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="4a089-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a089-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

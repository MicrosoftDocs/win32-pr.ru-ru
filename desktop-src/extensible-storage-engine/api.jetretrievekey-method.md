---
description: Дополнительные сведения о методе API. Жетретриевекэй
title: API. Жетретриевекэй, метод
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703246"
---
# <a name="apijetretrievekey-method"></a><span data-ttu-id="2451e-103">API. Жетретриевекэй, метод</span><span class="sxs-lookup"><span data-stu-id="2451e-103">Api.JetRetrieveKey method</span></span>

<span data-ttu-id="2451e-104">Возвращает ключ для записи индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="2451e-104">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="2451e-105">См. также [ретриевекэй (JET_SESID, JET_TABLEID, ретриевекэйгрбит)](./api.retrievekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="2451e-105">Also see [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span></span>

<span data-ttu-id="2451e-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2451e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2451e-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2451e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2451e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2451e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2451e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2451e-109">Parameters</span></span>

  - <span data-ttu-id="2451e-110">сесид</span><span class="sxs-lookup"><span data-stu-id="2451e-110">sesid</span></span>  
    <span data-ttu-id="2451e-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2451e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2451e-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="2451e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2451e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="2451e-113">tableid</span></span>  
    <span data-ttu-id="2451e-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2451e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2451e-115">Курсор, из которого извлекается ключ.</span><span class="sxs-lookup"><span data-stu-id="2451e-115">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="2451e-116">.</span><span class="sxs-lookup"><span data-stu-id="2451e-116">data</span></span>  
    <span data-ttu-id="2451e-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="2451e-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="2451e-118">Буфер, в который извлекается ключ.</span><span class="sxs-lookup"><span data-stu-id="2451e-118">The buffer to retrieve the key into.</span></span>

<!-- end list -->

  - <span data-ttu-id="2451e-119">dataSize</span><span class="sxs-lookup"><span data-stu-id="2451e-119">dataSize</span></span>  
    <span data-ttu-id="2451e-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2451e-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2451e-121">Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="2451e-121">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="2451e-122">актуалдатасизе</span><span class="sxs-lookup"><span data-stu-id="2451e-122">actualDataSize</span></span>  
    <span data-ttu-id="2451e-123">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2451e-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2451e-124">Возвращает фактический размер данных.</span><span class="sxs-lookup"><span data-stu-id="2451e-124">Returns the actual size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="2451e-125">грбит</span><span class="sxs-lookup"><span data-stu-id="2451e-125">grbit</span></span>  
    <span data-ttu-id="2451e-126">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевекэйгрбит](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2451e-126">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2451e-127">Получение параметров ключа.</span><span class="sxs-lookup"><span data-stu-id="2451e-127">Retrieve key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="2451e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2451e-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2451e-129">Справочник</span><span class="sxs-lookup"><span data-stu-id="2451e-129">Reference</span></span>

[<span data-ttu-id="2451e-130">Класс API</span><span class="sxs-lookup"><span data-stu-id="2451e-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2451e-131">Члены API</span><span class="sxs-lookup"><span data-stu-id="2451e-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2451e-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2451e-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

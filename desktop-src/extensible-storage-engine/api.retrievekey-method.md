---
description: Дополнительные сведения о методе API. Ретриевекэй
title: API. Ретриевекэй, метод
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcabab7639a9cf3128b0b2c314ba60c2de8f8e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808267"
---
# <a name="apiretrievekey-method"></a><span data-ttu-id="ec1be-103">API. Ретриевекэй, метод</span><span class="sxs-lookup"><span data-stu-id="ec1be-103">Api.RetrieveKey method</span></span>

<span data-ttu-id="ec1be-104">Возвращает ключ для записи индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="ec1be-104">Retrieves the key for the index entry at the current position of a cursor.</span></span>

<span data-ttu-id="ec1be-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec1be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec1be-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ec1be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec1be-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ec1be-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec1be-108">Parameters</span></span>

  - <span data-ttu-id="ec1be-109">сесид</span><span class="sxs-lookup"><span data-stu-id="ec1be-109">sesid</span></span>  
    <span data-ttu-id="ec1be-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ec1be-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ec1be-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="ec1be-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ec1be-112">TableID</span><span class="sxs-lookup"><span data-stu-id="ec1be-112">tableid</span></span>  
    <span data-ttu-id="ec1be-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ec1be-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ec1be-114">Курсор, из которого извлекается ключ.</span><span class="sxs-lookup"><span data-stu-id="ec1be-114">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ec1be-115">грбит</span><span class="sxs-lookup"><span data-stu-id="ec1be-115">grbit</span></span>  
    <span data-ttu-id="ec1be-116">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевекэйгрбит](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ec1be-116">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ec1be-117">Получение параметров ключа.</span><span class="sxs-lookup"><span data-stu-id="ec1be-117">Retrieve key options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ec1be-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec1be-118">Return value</span></span>

<span data-ttu-id="ec1be-119">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="ec1be-119">Type: \[\]</span></span>  
<span data-ttu-id="ec1be-120">Полученный ключ.</span><span class="sxs-lookup"><span data-stu-id="ec1be-120">The retrieved key.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ec1be-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec1be-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec1be-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="ec1be-122">Reference</span></span>

[<span data-ttu-id="ec1be-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="ec1be-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ec1be-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="ec1be-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ec1be-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ec1be-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

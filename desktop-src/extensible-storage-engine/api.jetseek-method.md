---
description: Дополнительные сведения о методе API. Жетсик
title: API. Жетсик, метод
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999551"
---
# <a name="apijetseek-method"></a><span data-ttu-id="4ea60-103">API. Жетсик, метод</span><span class="sxs-lookup"><span data-stu-id="4ea60-103">Api.JetSeek method</span></span>

<span data-ttu-id="4ea60-104">Эффективно позиционирует курсор на запись индекса, которая соответствует условиям поиска, заданным в ключе поиска в этом курсоре, и заданному неравенству.</span><span class="sxs-lookup"><span data-stu-id="4ea60-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="4ea60-105">Ключ поиска должен быть ранее создан с помощью [жетмакекэй (JET_SESID, JET_TABLEID, \[ \] , Int32, макекэйгрбит)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="4ea60-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="4ea60-106">См. также [трисик (JET_SESID, JET_TABLEID, сикгрбит)](./api.tryseek-method.md).</span><span class="sxs-lookup"><span data-stu-id="4ea60-106">Also see [TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span></span>

<span data-ttu-id="4ea60-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ea60-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ea60-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ea60-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea60-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ea60-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4ea60-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ea60-110">Parameters</span></span>

  - <span data-ttu-id="4ea60-111">сесид</span><span class="sxs-lookup"><span data-stu-id="4ea60-111">sesid</span></span>  
    <span data-ttu-id="4ea60-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ea60-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4ea60-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4ea60-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ea60-114">TableID</span><span class="sxs-lookup"><span data-stu-id="4ea60-114">tableid</span></span>  
    <span data-ttu-id="4ea60-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ea60-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4ea60-116">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="4ea60-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ea60-117">грбит</span><span class="sxs-lookup"><span data-stu-id="4ea60-117">grbit</span></span>  
    <span data-ttu-id="4ea60-118">Тип: [Microsoft. ISAM. ESENT. Interop. сикгрбит](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4ea60-118">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4ea60-119">Параметры поиска.</span><span class="sxs-lookup"><span data-stu-id="4ea60-119">Seek options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4ea60-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ea60-120">Return value</span></span>

<span data-ttu-id="4ea60-121">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4ea60-121">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="4ea60-122">Предупреждение ESENT.</span><span class="sxs-lookup"><span data-stu-id="4ea60-122">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ea60-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ea60-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ea60-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="4ea60-124">Reference</span></span>

[<span data-ttu-id="4ea60-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="4ea60-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4ea60-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="4ea60-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4ea60-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4ea60-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

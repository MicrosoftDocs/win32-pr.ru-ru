---
description: Дополнительные сведения о методе API. Жетпрепареупдате
title: API. Жетпрепареупдате, метод
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272541"
---
# <a name="apijetprepareupdate-method"></a><span data-ttu-id="ed0cb-103">API. Жетпрепареупдате, метод</span><span class="sxs-lookup"><span data-stu-id="ed0cb-103">Api.JetPrepareUpdate method</span></span>

<span data-ttu-id="ed0cb-104">Подготовка курсора к обновлению.</span><span class="sxs-lookup"><span data-stu-id="ed0cb-104">Prepare a cursor for update.</span></span>

<span data-ttu-id="ed0cb-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed0cb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed0cb-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed0cb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed0cb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="ed0cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed0cb-108">Parameters</span></span>

  - <span data-ttu-id="ed0cb-109">сесид</span><span class="sxs-lookup"><span data-stu-id="ed0cb-109">sesid</span></span>  
    <span data-ttu-id="ed0cb-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed0cb-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ed0cb-111">Сеанс, который запускает обновление.</span><span class="sxs-lookup"><span data-stu-id="ed0cb-111">The session which is starting the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed0cb-112">TableID</span><span class="sxs-lookup"><span data-stu-id="ed0cb-112">tableid</span></span>  
    <span data-ttu-id="ed0cb-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed0cb-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ed0cb-114">Курсор, для которого запускается обновление.</span><span class="sxs-lookup"><span data-stu-id="ed0cb-114">The cursor to start the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed0cb-115">подготовить</span><span class="sxs-lookup"><span data-stu-id="ed0cb-115">prep</span></span>  
    <span data-ttu-id="ed0cb-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ed0cb-116">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="ed0cb-117">Тип обновления для подготовки.</span><span class="sxs-lookup"><span data-stu-id="ed0cb-117">The type of update to prepare.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed0cb-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed0cb-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed0cb-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="ed0cb-119">Reference</span></span>

[<span data-ttu-id="ed0cb-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="ed0cb-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ed0cb-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="ed0cb-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ed0cb-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ed0cb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

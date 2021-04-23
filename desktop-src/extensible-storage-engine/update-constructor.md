---
description: 'Дополнительные сведения: конструктор обновлений'
title: Обновить конструктор
TOCTitle: 'Update constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.update(v=EXCHG.10)
ms:contentKeyID: 55104189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.Update
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 841403523e0cae7c71fb8fa0861c1d400a26a726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651082"
---
# <a name="update-constructor"></a><span data-ttu-id="8e858-103">Обновить конструктор</span><span class="sxs-lookup"><span data-stu-id="8e858-103">Update constructor</span></span>

<span data-ttu-id="8e858-104">Инициализирует новый экземпляр класса Update.</span><span class="sxs-lookup"><span data-stu-id="8e858-104">Initializes a new instance of the Update class.</span></span> <span data-ttu-id="8e858-105">Это автоматически начнет обновление.</span><span class="sxs-lookup"><span data-stu-id="8e858-105">This automatically begins an update.</span></span> <span data-ttu-id="8e858-106">Обновление будет отменено, если не было явно сохранено.</span><span class="sxs-lookup"><span data-stu-id="8e858-106">The update will be cancelled if not explicitly saved.</span></span>

<span data-ttu-id="8e858-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e858-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e858-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e858-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e858-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e858-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prep

Dim instance As New Update(sesid, tableid, _
    prep)
```

``` csharp
public Update(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="8e858-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e858-110">Parameters</span></span>

  - <span data-ttu-id="8e858-111">сесид</span><span class="sxs-lookup"><span data-stu-id="8e858-111">sesid</span></span>  
    <span data-ttu-id="8e858-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e858-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8e858-113">Сеанс, для которого запускается транзакция.</span><span class="sxs-lookup"><span data-stu-id="8e858-113">The session to start the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e858-114">TableID</span><span class="sxs-lookup"><span data-stu-id="8e858-114">tableid</span></span>  
    <span data-ttu-id="8e858-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e858-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8e858-116">TableID для подготовки обновления для.</span><span class="sxs-lookup"><span data-stu-id="8e858-116">The tableid to prepare the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e858-117">подготовить</span><span class="sxs-lookup"><span data-stu-id="8e858-117">prep</span></span>  
    <span data-ttu-id="8e858-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8e858-118">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="8e858-119">Тип обновления.</span><span class="sxs-lookup"><span data-stu-id="8e858-119">The type of update.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e858-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e858-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e858-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="8e858-121">Reference</span></span>

[<span data-ttu-id="8e858-122">Класс обновления</span><span class="sxs-lookup"><span data-stu-id="8e858-122">Update class</span></span>](./update-class.md)

[<span data-ttu-id="8e858-123">Обновить элементы</span><span class="sxs-lookup"><span data-stu-id="8e858-123">Update members</span></span>](./update-members.md)

[<span data-ttu-id="8e858-124">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8e858-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

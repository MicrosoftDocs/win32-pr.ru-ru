---
description: Дополнительные сведения о методе API. Жетклосетабле
title: API. Жетклосетабле, метод
TOCTitle: 'JetCloseTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosetable(v=EXCHG.10)
ms:contentKeyID: 55100664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fee4ad7d7accf71bd4c3439f954ee36badd2ea20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990998"
---
# <a name="apijetclosetable-method"></a><span data-ttu-id="63fe9-103">API. Жетклосетабле, метод</span><span class="sxs-lookup"><span data-stu-id="63fe9-103">Api.JetCloseTable method</span></span>

<span data-ttu-id="63fe9-104">Закройте открытую таблицу.</span><span class="sxs-lookup"><span data-stu-id="63fe9-104">Close an open table.</span></span>

<span data-ttu-id="63fe9-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="63fe9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="63fe9-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="63fe9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="63fe9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63fe9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseTable ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetCloseTable(sesid, tableid)
```

``` csharp
public static void JetCloseTable(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="63fe9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63fe9-108">Parameters</span></span>

  - <span data-ttu-id="63fe9-109">сесид</span><span class="sxs-lookup"><span data-stu-id="63fe9-109">sesid</span></span>  
    <span data-ttu-id="63fe9-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="63fe9-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="63fe9-111">Сеанс, в котором была открыта таблица.</span><span class="sxs-lookup"><span data-stu-id="63fe9-111">The session which opened the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="63fe9-112">TableID</span><span class="sxs-lookup"><span data-stu-id="63fe9-112">tableid</span></span>  
    <span data-ttu-id="63fe9-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="63fe9-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="63fe9-114">Таблица, которую нужно закрыть.</span><span class="sxs-lookup"><span data-stu-id="63fe9-114">The table to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="63fe9-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63fe9-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="63fe9-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="63fe9-116">Reference</span></span>

[<span data-ttu-id="63fe9-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="63fe9-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="63fe9-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="63fe9-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="63fe9-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="63fe9-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

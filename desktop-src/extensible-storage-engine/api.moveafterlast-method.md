---
description: Дополнительные сведения о методе API. Мовеафтерласт
title: API. Мовеафтерласт, метод
TOCTitle: 'MoveAfterLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveAfterLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.moveafterlast(v=EXCHG.10)
ms:contentKeyID: 55100851
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveAfterLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37d3e4eae32c9540f3ee469e4b782c893aa15c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703307"
---
# <a name="apimoveafterlast-method"></a><span data-ttu-id="92acb-103">API. Мовеафтерласт, метод</span><span class="sxs-lookup"><span data-stu-id="92acb-103">Api.MoveAfterLast method</span></span>

<span data-ttu-id="92acb-104">Поместите курсор после последней записи в таблице.</span><span class="sxs-lookup"><span data-stu-id="92acb-104">Position the cursor after the last record in the table.</span></span> <span data-ttu-id="92acb-105">Последующее перемещение предыдущего положения курсора будет размещено на последней записи.</span><span class="sxs-lookup"><span data-stu-id="92acb-105">A subsequent move previous will position the cursor on the last record.</span></span>

<span data-ttu-id="92acb-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92acb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92acb-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92acb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92acb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92acb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveAfterLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveAfterLast(sesid, tableid)
```

``` csharp
public static void MoveAfterLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="92acb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92acb-109">Parameters</span></span>

  - <span data-ttu-id="92acb-110">сесид</span><span class="sxs-lookup"><span data-stu-id="92acb-110">sesid</span></span>  
    <span data-ttu-id="92acb-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92acb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="92acb-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="92acb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="92acb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="92acb-113">tableid</span></span>  
    <span data-ttu-id="92acb-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92acb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="92acb-115">Таблица для размещения.</span><span class="sxs-lookup"><span data-stu-id="92acb-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="92acb-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92acb-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92acb-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="92acb-117">Reference</span></span>

[<span data-ttu-id="92acb-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="92acb-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="92acb-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="92acb-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="92acb-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="92acb-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
description: Дополнительные сведения о методе API. Жетделете
title: API. Жетделете, метод
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897010"
---
# <a name="apijetdelete-method"></a><span data-ttu-id="535af-103">API. Жетделете, метод</span><span class="sxs-lookup"><span data-stu-id="535af-103">Api.JetDelete method</span></span>

<span data-ttu-id="535af-104">Удаляет текущую запись в таблице базы данных.</span><span class="sxs-lookup"><span data-stu-id="535af-104">Deletes the current record in a database table.</span></span>

<span data-ttu-id="535af-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="535af-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="535af-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="535af-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="535af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="535af-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="535af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="535af-108">Parameters</span></span>

  - <span data-ttu-id="535af-109">сесид</span><span class="sxs-lookup"><span data-stu-id="535af-109">sesid</span></span>  
    <span data-ttu-id="535af-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="535af-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="535af-111">Сеанс, открывший курсор.</span><span class="sxs-lookup"><span data-stu-id="535af-111">The session that opened the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="535af-112">TableID</span><span class="sxs-lookup"><span data-stu-id="535af-112">tableid</span></span>  
    <span data-ttu-id="535af-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="535af-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="535af-114">Курсор в таблице базы данных.</span><span class="sxs-lookup"><span data-stu-id="535af-114">The cursor on a database table.</span></span> <span data-ttu-id="535af-115">Текущая строка будет удалена.</span><span class="sxs-lookup"><span data-stu-id="535af-115">The current row will be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="535af-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="535af-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="535af-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="535af-117">Reference</span></span>

[<span data-ttu-id="535af-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="535af-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="535af-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="535af-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="535af-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="535af-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

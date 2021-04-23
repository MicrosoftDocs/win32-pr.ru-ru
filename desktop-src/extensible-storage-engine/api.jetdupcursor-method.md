---
description: Дополнительные сведения о методе API. Жетдупкурсор
title: API. Жетдупкурсор, метод
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540866"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="677c7-103">API. Жетдупкурсор, метод</span><span class="sxs-lookup"><span data-stu-id="677c7-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="677c7-104">Дублирует открытый курсор и возвращает указатель на дублирующийся курсор.</span><span class="sxs-lookup"><span data-stu-id="677c7-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="677c7-105">Если курсор, который был продублирован, был курсором только для чтения, то дубликат курсора также является курсором только для чтения.</span><span class="sxs-lookup"><span data-stu-id="677c7-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="677c7-106">Любое состояние, связанное с построением ключа поиска или обновлением записи, не копируется в дублирующийся курсор.</span><span class="sxs-lookup"><span data-stu-id="677c7-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="677c7-107">Кроме того, положение исходного курсора не дублируется в повторяющемся курсоре.</span><span class="sxs-lookup"><span data-stu-id="677c7-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="677c7-108">Дубликат курсора всегда открывается в кластеризованном индексе, и его расположение всегда находится в первой строке таблицы.</span><span class="sxs-lookup"><span data-stu-id="677c7-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="677c7-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="677c7-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="677c7-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="677c7-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="677c7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="677c7-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="677c7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="677c7-112">Parameters</span></span>

  - <span data-ttu-id="677c7-113">сесид</span><span class="sxs-lookup"><span data-stu-id="677c7-113">sesid</span></span>  
    <span data-ttu-id="677c7-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="677c7-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="677c7-115">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="677c7-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="677c7-116">TableID</span><span class="sxs-lookup"><span data-stu-id="677c7-116">tableid</span></span>  
    <span data-ttu-id="677c7-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="677c7-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="677c7-118">Дублирующий курсор.</span><span class="sxs-lookup"><span data-stu-id="677c7-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="677c7-119">невтаблеид</span><span class="sxs-lookup"><span data-stu-id="677c7-119">newTableid</span></span>  
    <span data-ttu-id="677c7-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="677c7-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="677c7-121">Дублирующийся курсор.</span><span class="sxs-lookup"><span data-stu-id="677c7-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="677c7-122">грбит</span><span class="sxs-lookup"><span data-stu-id="677c7-122">grbit</span></span>  
    <span data-ttu-id="677c7-123">Тип: [Microsoft. ISAM. ESENT. Interop. дупкурсоргрбит](./dupcursorgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="677c7-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="677c7-124">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="677c7-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="677c7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="677c7-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="677c7-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="677c7-126">Reference</span></span>

[<span data-ttu-id="677c7-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="677c7-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="677c7-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="677c7-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="677c7-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="677c7-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

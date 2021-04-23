---
description: 'Дополнительные сведения о методе: Server2003Api. JetUpdate2'
title: Server2003Api. JetUpdate2, метод (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143510"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="bc8da-103">Server2003Api. JetUpdate2, метод</span><span class="sxs-lookup"><span data-stu-id="bc8da-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="bc8da-104">Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки.</span><span class="sxs-lookup"><span data-stu-id="bc8da-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="bc8da-105">Удаление строки таблицы выполняется путем вызова [жетделете (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="bc8da-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="bc8da-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc8da-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="bc8da-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc8da-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc8da-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bc8da-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc8da-109">Parameters</span></span>

  - <span data-ttu-id="bc8da-110">сесид</span><span class="sxs-lookup"><span data-stu-id="bc8da-110">sesid</span></span>  
    <span data-ttu-id="bc8da-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc8da-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bc8da-112">Сеанс, который запустил обновление.</span><span class="sxs-lookup"><span data-stu-id="bc8da-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8da-113">TableID</span><span class="sxs-lookup"><span data-stu-id="bc8da-113">tableid</span></span>  
    <span data-ttu-id="bc8da-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc8da-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bc8da-115">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="bc8da-115">The cursor to update.</span></span> <span data-ttu-id="bc8da-116">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="bc8da-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8da-117">закладка</span><span class="sxs-lookup"><span data-stu-id="bc8da-117">bookmark</span></span>  
    <span data-ttu-id="bc8da-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="bc8da-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="bc8da-119">Возвращает закладку обновленной записи.</span><span class="sxs-lookup"><span data-stu-id="bc8da-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="bc8da-120">Может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bc8da-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8da-121">букмарксизе</span><span class="sxs-lookup"><span data-stu-id="bc8da-121">bookmarkSize</span></span>  
    <span data-ttu-id="bc8da-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bc8da-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bc8da-123">Размер буфера закладок.</span><span class="sxs-lookup"><span data-stu-id="bc8da-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8da-124">актуалбукмарксизе</span><span class="sxs-lookup"><span data-stu-id="bc8da-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="bc8da-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bc8da-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bc8da-126">Возвращает фактический размер закладки.</span><span class="sxs-lookup"><span data-stu-id="bc8da-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc8da-127">грбит</span><span class="sxs-lookup"><span data-stu-id="bc8da-127">grbit</span></span>  
    <span data-ttu-id="bc8da-128">Тип: [Microsoft. ISAM. ESENT. Interop. server2003. упдатегрбит](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bc8da-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bc8da-129">Параметры обновления.</span><span class="sxs-lookup"><span data-stu-id="bc8da-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8da-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc8da-130">Remarks</span></span>

<span data-ttu-id="bc8da-131">Жетупдате является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="bc8da-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="bc8da-132">Обновление начинается с вызова [жетпрепареупдате (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , а затем путем вызова [жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, сетколумнгрбит, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="bc8da-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="bc8da-133">Наконец, \[ \] для завершения операции обновления вызывается JetUpdate2 (JET_SESID, JET_TABLEID,, Int32, Int32, упдатегрбит).</span><span class="sxs-lookup"><span data-stu-id="bc8da-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="bc8da-134">Индексы обновляются только в Жетупдате или, а не во время Жетсетколумн.</span><span class="sxs-lookup"><span data-stu-id="bc8da-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc8da-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc8da-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc8da-136">Справочник</span><span class="sxs-lookup"><span data-stu-id="bc8da-136">Reference</span></span>

[<span data-ttu-id="bc8da-137">Класс Server2003Api</span><span class="sxs-lookup"><span data-stu-id="bc8da-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="bc8da-138">Элементы Server2003Api</span><span class="sxs-lookup"><span data-stu-id="bc8da-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="bc8da-139">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="bc8da-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

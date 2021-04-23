---
description: 'Дополнительные сведения: метод API. Жетупдате (JET_SESID, JET_TABLEID, Byte, Int32, Int32)'
title: Метод API. Жетупдате (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897986"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="6c83f-103">Метод API. Жетупдате (JET_SESID, JET_TABLEID, Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="6c83f-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="6c83f-104">Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки.</span><span class="sxs-lookup"><span data-stu-id="6c83f-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="6c83f-105">Удаление строки таблицы выполняется путем вызова [жетделете (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="6c83f-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="6c83f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c83f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c83f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c83f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c83f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c83f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="6c83f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c83f-109">Parameters</span></span>

  - <span data-ttu-id="6c83f-110">сесид</span><span class="sxs-lookup"><span data-stu-id="6c83f-110">sesid</span></span>  
    <span data-ttu-id="6c83f-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c83f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6c83f-112">Сеанс, который запустил обновление.</span><span class="sxs-lookup"><span data-stu-id="6c83f-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c83f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6c83f-113">tableid</span></span>  
    <span data-ttu-id="6c83f-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c83f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6c83f-115">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="6c83f-115">The cursor to update.</span></span> <span data-ttu-id="6c83f-116">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="6c83f-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c83f-117">закладка</span><span class="sxs-lookup"><span data-stu-id="6c83f-117">bookmark</span></span>  
    <span data-ttu-id="6c83f-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="6c83f-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="6c83f-119">Возвращает закладку обновленной записи.</span><span class="sxs-lookup"><span data-stu-id="6c83f-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="6c83f-120">Может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="6c83f-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c83f-121">букмарксизе</span><span class="sxs-lookup"><span data-stu-id="6c83f-121">bookmarkSize</span></span>  
    <span data-ttu-id="6c83f-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6c83f-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6c83f-123">Размер буфера закладок.</span><span class="sxs-lookup"><span data-stu-id="6c83f-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c83f-124">актуалбукмарксизе</span><span class="sxs-lookup"><span data-stu-id="6c83f-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="6c83f-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6c83f-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6c83f-126">Возвращает фактический размер закладки.</span><span class="sxs-lookup"><span data-stu-id="6c83f-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c83f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c83f-127">Remarks</span></span>

<span data-ttu-id="6c83f-128">Жетупдате является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="6c83f-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="6c83f-129">Обновление начинается с вызова [жетпрепареупдате (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , а затем путем вызова [жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, сетколумнгрбит, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="6c83f-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="6c83f-130">Наконец, \[ \] для завершения операции обновления вызывается жетупдате (JET_SESID, JET_TABLEID,, Int32, Int32).</span><span class="sxs-lookup"><span data-stu-id="6c83f-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="6c83f-131">Индексы обновляются только в Жетупдате или, а не во время Жетсетколумн.</span><span class="sxs-lookup"><span data-stu-id="6c83f-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c83f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c83f-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c83f-133">Справочник</span><span class="sxs-lookup"><span data-stu-id="6c83f-133">Reference</span></span>

[<span data-ttu-id="6c83f-134">Класс API</span><span class="sxs-lookup"><span data-stu-id="6c83f-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6c83f-135">Члены API</span><span class="sxs-lookup"><span data-stu-id="6c83f-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6c83f-136">Перегрузка Жетупдате</span><span class="sxs-lookup"><span data-stu-id="6c83f-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="6c83f-137">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6c83f-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

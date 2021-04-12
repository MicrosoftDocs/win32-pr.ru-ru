---
description: 'Дополнительные сведения: метод API. Жетупдате (JET_SESID, JET_TABLEID)'
title: Метод API. Жетупдате (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349585"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="fa49c-103">Метод API. Жетупдате (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="fa49c-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="fa49c-104">Функция Жетупдате выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки.</span><span class="sxs-lookup"><span data-stu-id="fa49c-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="fa49c-105">Удаление строки таблицы выполняется путем вызова [жетделете (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa49c-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="fa49c-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa49c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fa49c-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fa49c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa49c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa49c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="fa49c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa49c-109">Parameters</span></span>

  - <span data-ttu-id="fa49c-110">сесид</span><span class="sxs-lookup"><span data-stu-id="fa49c-110">sesid</span></span>  
    <span data-ttu-id="fa49c-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fa49c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fa49c-112">Сеанс, который запустил обновление.</span><span class="sxs-lookup"><span data-stu-id="fa49c-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa49c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="fa49c-113">tableid</span></span>  
    <span data-ttu-id="fa49c-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fa49c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fa49c-115">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="fa49c-115">The cursor to update.</span></span> <span data-ttu-id="fa49c-116">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="fa49c-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa49c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa49c-117">Remarks</span></span>

<span data-ttu-id="fa49c-118">Жетупдате является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="fa49c-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="fa49c-119">Обновление начинается с вызова [жетпрепареупдате (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , а затем путем вызова [жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, сетколумнгрбит, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="fa49c-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="fa49c-120">Наконец, для завершения операции обновления вызывается [жетупдате (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) .</span><span class="sxs-lookup"><span data-stu-id="fa49c-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="fa49c-121">Индексы обновляются только в Жетупдате или, а не во время Жетсетколумн.</span><span class="sxs-lookup"><span data-stu-id="fa49c-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa49c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa49c-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa49c-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="fa49c-123">Reference</span></span>

[<span data-ttu-id="fa49c-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="fa49c-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fa49c-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="fa49c-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fa49c-126">Перегрузка Жетупдате</span><span class="sxs-lookup"><span data-stu-id="fa49c-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="fa49c-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fa49c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

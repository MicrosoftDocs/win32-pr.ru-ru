---
description: 'Дополнительные сведения: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712437"
---
# <a name="jet_ls"></a><span data-ttu-id="7dcbc-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-103">JET_LS</span></span>


<span data-ttu-id="7dcbc-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7dcbc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="7dcbc-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-105">JET_LS</span></span>

<span data-ttu-id="7dcbc-106">**JET_LS** тип данных содержит контекстный обработчик для локального хранилища (Ls). Этот маркер может быть связан с курсором или таблицей и может ссылаться на динамически выделенные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="7dcbc-107">**Windows XP: JET_LS** введен в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="7dcbc-108">Типы данных</span><span class="sxs-lookup"><span data-stu-id="7dcbc-108">Data Types</span></span>

<span data-ttu-id="7dcbc-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="7dcbc-109">JET_LS</span></span>

<span data-ttu-id="7dcbc-110">Значение JET_LSNil указывает на недопустимый обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="7dcbc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7dcbc-111">Remarks</span></span>

<span data-ttu-id="7dcbc-112">Обработчик контекста изначально связан с типом данных **JET_LS** с помощью [жетсетлс](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="7dcbc-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="7dcbc-113">Маркер контекста можно извлечь из типа данных **JET_LS** с помощью [жетжетлс](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="7dcbc-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="7dcbc-114">Обработчик контекста может быть явно связан с типом данных **JET_LS** с помощью [жетжетлс](./jetgetls-function.md) с JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="7dcbc-115">Кроме того, маркер контекста может быть неявно связан с типом данных **JET_LS** , когда базовый объект освобождается ядром СУБД в результате прямого или непрямого действия приложения.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="7dcbc-116">В неявном случае для приложения выдается обратный вызов времени выполнения, чтобы он мог очистить контекстный маркер.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="7dcbc-117">Дополнительные сведения о неявном разрыве связи с типом данных **JET_LS** см. в разделе [жетсетлс](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="7dcbc-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="7dcbc-118">С типом данных JET_LS связаны следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7dcbc-119">Термин</span><span class="sxs-lookup"><span data-stu-id="7dcbc-119">Term</span></span></p></th>
<th><p><span data-ttu-id="7dcbc-120">Описание</span><span class="sxs-lookup"><span data-stu-id="7dcbc-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dcbc-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="7dcbc-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="7dcbc-122">Маркер контекста не связан с объектом.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dcbc-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="7dcbc-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="7dcbc-124">Задает или получает локальное хранилище, связанное с курсором таблицы.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dcbc-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="7dcbc-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="7dcbc-126">Задайте или получите локальное хранилище, связанное с таблицей.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dcbc-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="7dcbc-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="7dcbc-128">Недопустимый маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="7dcbc-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7dcbc-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dcbc-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="7dcbc-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcbc-131">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dcbc-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7dcbc-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcbc-133">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dcbc-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7dcbc-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7dcbc-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="7dcbc-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7dcbc-136">См. также:</span><span class="sxs-lookup"><span data-stu-id="7dcbc-136">See Also</span></span>

[<span data-ttu-id="7dcbc-137">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="7dcbc-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="7dcbc-138">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="7dcbc-138">JetGetLS</span></span>](./jetgetls-function.md)

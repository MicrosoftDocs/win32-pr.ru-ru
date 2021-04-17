---
description: 'Дополнительные сведения: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
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
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674233"
---
# <a name="jet_cbtyp"></a><span data-ttu-id="31447-103">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="31447-103">JET_CBTYP</span></span>


<span data-ttu-id="31447-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="31447-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_cbtyp"></a><span data-ttu-id="31447-105">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="31447-105">JET_CBTYP</span></span>

<span data-ttu-id="31447-106">**JET_CBTYP** группа констант описывает все возможные точки в операции, которые ядро СУБД будет уведомлять приложение путем вызова функции обратного вызова [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="31447-106">The **JET_CBTYP** group of constants describes all possible points in an operation that the database engine will notify an application by calling the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span> <span data-ttu-id="31447-107">Ядро СУБД передает одну из этих констант в параметр *кбтип* функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="31447-107">The database engine passes one of these constants in the *cbtyp* parameter of the callback function.</span></span> <span data-ttu-id="31447-108">Значение других параметров, передаваемых ядром СУБД в этом вызове, зависит от конкретного **JET_CBTYP** .</span><span class="sxs-lookup"><span data-stu-id="31447-108">The meaning of the other parameters passed by the database engine in this call depend on the specific **JET_CBTYP** passed.</span></span>

<span data-ttu-id="31447-109">**Windows XP:**  **JET_CBTYP** группа констант введена в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31447-109">**Windows XP:**  The **JET_CBTYP** group of constants are introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31447-110">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="31447-110">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="31447-111">Описание</span><span class="sxs-lookup"><span data-stu-id="31447-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31447-112">JET_cbtypNull</span><span class="sxs-lookup"><span data-stu-id="31447-112">JET_cbtypNull</span></span><br />
<span data-ttu-id="31447-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31447-113">0x00000000</span></span></p></td>
<td><p><span data-ttu-id="31447-114">Этот обратный вызов зарезервирован и всегда считается недопустимым.</span><span class="sxs-lookup"><span data-stu-id="31447-114">This callback is reserved and always considered invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-115">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="31447-115">JET_cbtypFinalize</span></span><br />
<span data-ttu-id="31447-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="31447-116">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="31447-117">Этот обратный вызов зарезервирован для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="31447-117">This callback is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31447-118">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="31447-118">JET_cbtypBeforeInsert</span></span><br />
<span data-ttu-id="31447-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="31447-119">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="31447-120">Этот обратный вызов выполняется непосредственно перед вставкой новой записи в таблицу с помощью вызова <a href="gg269288(v=exchg.10).md">жетупдате</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-120">This callback will occur just before a new record is inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="31447-121">Указатель функции для этой причины обратного вызова либо передается в <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , либо настраивается во время выполнения с помощью <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-121">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="31447-122">Дополнительные сведения см. в разделе <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-122">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-123">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-123">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-124"><em>сесид</em>: сеанс, в котором находится Вставляемая запись.</span><span class="sxs-lookup"><span data-stu-id="31447-124"><em>sesid</em>: The session that has the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="31447-125"><em>DBID</em>: идентификатор базы данных таблицы, содержащей вставляемую запись.</span><span class="sxs-lookup"><span data-stu-id="31447-125"><em>dbid</em>: The database ID of the table that contains the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="31447-126"><em>tableid</em>: курсор, подготовленный для вставки новой вставляемой записи.</span><span class="sxs-lookup"><span data-stu-id="31447-126"><em>tableid</em>: The cursor that has prepared the new record to be inserted.</span></span> <span data-ttu-id="31447-127">Важно отметить, что в данный момент значения всех столбцов версии или автоинкремента могут быть неправильными.</span><span class="sxs-lookup"><span data-stu-id="31447-127">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="31447-128"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-128"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-129"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-129"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-130"><em>пвконтекст</em>: указатель контекста передается в <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a> или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="31447-130"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="31447-131"><em>улунусед</em>: <strong>null</strong> если функция обратного вызова возвращает ошибку, то операция, исходящий обратный вызов, завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="31447-131"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-132">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="31447-132">JET_cbtypAfterInsert</span></span><br />
<span data-ttu-id="31447-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="31447-133">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="31447-134">Этот обратный вызов выполняется сразу после вставки новой записи в таблицу с помощью вызова <a href="gg269288(v=exchg.10).md">жетупдате</a> , но до того, как <a href="gg269288(v=exchg.10).md">жетупдате</a> возвращается вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="31447-134">This callback will occur just after a new record has been inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but before <a href="gg269288(v=exchg.10).md">JetUpdate</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="31447-135">Указатель функции для этой причины обратного вызова либо передается в <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , либо настраивается во время выполнения с помощью <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-135">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="31447-136">Дополнительные сведения см. в разделе <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-136">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-137">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-137">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-138"><em>сесид</em>: сеанс, содержащий только что вставленную запись.</span><span class="sxs-lookup"><span data-stu-id="31447-138"><em>sesid</em>: The session that has the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="31447-139"><em>DBID</em>: идентификатор базы данных таблицы, содержащей только что вставленную запись.</span><span class="sxs-lookup"><span data-stu-id="31447-139"><em>dbid</em>: The database ID of the table that contains the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="31447-140"><em>tableid</em>: курсор на таблицу, в которую вставлена запись.</span><span class="sxs-lookup"><span data-stu-id="31447-140"><em>tableid</em>: A cursor on the table into which the record that was just inserted.</span></span> <span data-ttu-id="31447-141">Обратите внимание, что курсор по-прежнему находится в той же записи индекса, что и в обратном вызове перед вставкой.</span><span class="sxs-lookup"><span data-stu-id="31447-141">Note that the cursor is still positioned on the same index entry as it was in the before insert callback.</span></span> <span data-ttu-id="31447-142">Обратите внимание, что эта запись индекса не может быть связана ни с одной из способов вставки записи.</span><span class="sxs-lookup"><span data-stu-id="31447-142">Further note that this index entry may not be related in any way to the record being inserted.</span></span></p></li>
<li><p><span data-ttu-id="31447-143"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-143"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-144"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-144"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-145"><em>пвконтекст</em>: указатель контекста передается в <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a> или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="31447-145"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="31447-146"><em>улунусед</em>: <strong>null</strong> если функция обратного вызова возвращает ошибку, она будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="31447-146"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31447-147">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="31447-147">JET_cbtypBeforeReplace</span></span><br />
<span data-ttu-id="31447-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="31447-148">0x00000008</span></span></p></td>
<td><p><span data-ttu-id="31447-149">Этот обратный вызов выполняется непосредственно перед существующей записью в таблице, измененной с помощью вызова <a href="gg269288(v=exchg.10).md">жетупдате</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-149">This callback will occur just prior to an existing record in a table being changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="31447-150">Указатель функции для этой причины обратного вызова либо передается в <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , либо настраивается во время выполнения с помощью <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-150">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="31447-151">Дополнительные сведения см. в разделе <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-151">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-152">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-152">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-153"><em>сесид</em>: сеанс с изменяемой записью.</span><span class="sxs-lookup"><span data-stu-id="31447-153"><em>sesid</em>: The session that has the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="31447-154"><em>DBID</em>: идентификатор базы данных таблицы, содержащей изменяемую запись.</span><span class="sxs-lookup"><span data-stu-id="31447-154"><em>dbid</em>: The database ID of the table that contains the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="31447-155"><em>tableid</em>: курсор, расположенный на записи индекса, связанной с изменяемой записью.</span><span class="sxs-lookup"><span data-stu-id="31447-155"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be changed.</span></span> <span data-ttu-id="31447-156">Важно отметить, что в данный момент значения всех столбцов версии или автоинкремента могут быть неправильными.</span><span class="sxs-lookup"><span data-stu-id="31447-156">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="31447-157"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-157"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-158"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-158"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-159"><em>пвконтекст</em>: указатель контекста передается в <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a> или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="31447-159"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="31447-160"><em>улунусед</em>: <strong>null</strong> если функция обратного вызова возвращает ошибку, то операция, исходящий обратный вызов, завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="31447-160"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-161">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="31447-161">JET_cbtypAfterReplace</span></span><br />
<span data-ttu-id="31447-162">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31447-162">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="31447-163">Этот обратный вызов происходит сразу после того, как существующая запись в таблице была изменена вызовом <a href="gg269288(v=exchg.10).md">жетупдате</a> , но до <a href="gg269288(v=exchg.10).md">жетупдате</a> , возвращая ее вызывающему.</span><span class="sxs-lookup"><span data-stu-id="31447-163">This callback will occur just after an existing record in a table has been changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but prior to <a href="gg269288(v=exchg.10).md">JetUpdate</a> returning to its caller.</span></span></p>
<p><span data-ttu-id="31447-164">Указатель функции для этой причины обратного вызова либо передается в <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , либо настраивается во время выполнения с помощью <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-164">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="31447-165">Дополнительные сведения см. в разделе <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-165">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-166">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-166">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-167"><em>сесид</em>: сеанс с только что измененной записью.</span><span class="sxs-lookup"><span data-stu-id="31447-167"><em>sesid</em>: The session that has the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="31447-168"><em>DBID</em>: идентификатор базы данных таблицы, содержащей только что измененную запись.</span><span class="sxs-lookup"><span data-stu-id="31447-168"><em>dbid</em>: The database ID of the table that contains the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="31447-169"><em>tableid</em>: курсор, расположенный на элементе индекса, связанном с записью, которая была только что изменена.</span><span class="sxs-lookup"><span data-stu-id="31447-169"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="31447-170"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-170"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-171"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-171"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-172"><em>пвконтекст</em>: указатель контекста передается в <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a> или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="31447-172"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="31447-173"><em>улунусед</em>: <strong>null</strong> если функция обратного вызова возвращает ошибку, она будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="31447-173"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31447-174">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="31447-174">JET_cbtypBeforeDelete</span></span><br />
<span data-ttu-id="31447-175">0x00000020</span><span class="sxs-lookup"><span data-stu-id="31447-175">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="31447-176">Этот обратный вызов выполняется непосредственно перед удалением существующей записи в таблице путем вызова <a href="gg269315(v=exchg.10).md">жетделете</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-176">This callback will occur just before an existing record in a table is deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span></span></p>
<p><span data-ttu-id="31447-177">Указатель функции для этой причины обратного вызова либо передается в <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , либо настраивается во время выполнения с помощью <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-177">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="31447-178">Дополнительные сведения см. в разделе <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-178">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-179">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-179">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-180"><em>сесид</em>: сеанс, в котором находится удаляемая запись.</span><span class="sxs-lookup"><span data-stu-id="31447-180"><em>sesid</em>: The session that has the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="31447-181"><em>DBID</em>: идентификатор базы данных таблицы, содержащей удаляемую запись.</span><span class="sxs-lookup"><span data-stu-id="31447-181"><em>dbid</em>: The database ID of the table that contains the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="31447-182"><em>tableid</em>: курсор, расположенный на записи индекса, связанной с удаляемой записью.</span><span class="sxs-lookup"><span data-stu-id="31447-182"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="31447-183"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-183"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-184"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-184"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-185"><em>пвконтекст</em>: указатель контекста передается в <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a> или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="31447-185"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="31447-186"><em>улунусед</em>: <strong>null</strong> если функция обратного вызова возвращает ошибку, то операция, исходящий обратный вызов, завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="31447-186"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-187">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="31447-187">JET_cbtypAfterDelete</span></span><br />
<span data-ttu-id="31447-188">0x00000040</span><span class="sxs-lookup"><span data-stu-id="31447-188">0x00000040</span></span></p></td>
<td><p><span data-ttu-id="31447-189">Этот обратный вызов происходит сразу после удаления существующей записи в таблице с помощью вызова <a href="gg269315(v=exchg.10).md">жетделете</a> , но до того, как <a href="gg269315(v=exchg.10).md">жетделете</a> возвращается вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="31447-189">This callback will occur just after an existing record in a table has been deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a> but before <a href="gg269315(v=exchg.10).md">JetDelete</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="31447-190">Указатель функции для этой причины обратного вызова либо передается в <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , либо настраивается во время выполнения с помощью <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-190">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="31447-191">Дополнительные сведения см. в разделе <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-191">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-192">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-192">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-193"><em>сесид</em>: сеанс, в котором есть только что удаленная запись.</span><span class="sxs-lookup"><span data-stu-id="31447-193"><em>sesid</em>: The session that has the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="31447-194"><em>DBID</em>: идентификатор базы данных таблицы, содержащей только что удаленную запись.</span><span class="sxs-lookup"><span data-stu-id="31447-194"><em>dbid</em>: The database ID of the table that contains the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="31447-195"><em>tableid</em>: курсор, расположенный на элементе индекса, связанном с записью, которая была только что удалена.</span><span class="sxs-lookup"><span data-stu-id="31447-195"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="31447-196"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-196"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-197"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-197"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-198"><em>пвконтекст</em>: указатель контекста передается в <a href="gg269175(v=exchg.10).md">жетрегистеркаллбакк</a> или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="31447-198"><em>pvContext</em>: the context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="31447-199"><em>улунусед</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-199"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="31447-200">Если обратный вызов возвращает ошибку, она будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="31447-200">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31447-201">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="31447-201">JET_cbtypUserDefinedDefaultValue</span></span><br />
<span data-ttu-id="31447-202">0x00000080</span><span class="sxs-lookup"><span data-stu-id="31447-202">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="31447-203">Этот обратный вызов выполняется, когда подсистеме требуется получить определенное пользователем значение столбца из приложения.</span><span class="sxs-lookup"><span data-stu-id="31447-203">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="31447-204">Этот обратный вызов по сути является ограниченной реализацией <a href="gg269198(v=exchg.10).md">жетретриевеколумн</a> , которая оценивается приложением.</span><span class="sxs-lookup"><span data-stu-id="31447-204">This callback is essentially a limited implementation of <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> that is evaluated by the application.</span></span> <span data-ttu-id="31447-205">Для определяемого пользователем значения по умолчанию может быть возвращено не более одного значения столбца.</span><span class="sxs-lookup"><span data-stu-id="31447-205">A maximum of one column value can be returned for a user defined default value.</span></span></p>
<p><span data-ttu-id="31447-206">Указатель функции для этой причины обратного вызова либо передается в <a href="gg294122(v=exchg.10).md">жетаддколумн</a> с помощью структуры <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , либо передается <a href="gg269343(v=exchg.10).md">жеткреатетаблеколумниндекс</a> с помощью структуры <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> в структуре <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> структуры <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="31447-206">The function pointer for this callback reason is either passed to <a href="gg294122(v=exchg.10).md">JetAddColumn</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure or passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure in a <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure in a <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure.</span></span></p>
<p><span data-ttu-id="31447-207">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-207">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-208"><em>сесид</em>: сеанс, который вычисляет определяемое пользователем значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31447-208"><em>sesid</em>: The session that is computing the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="31447-209"><em>DBID</em>: идентификатор базы данных таблицы, которая содержит определенное пользователем значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="31447-209"><em>dbid</em>: The database ID of the table that contains the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="31447-210"><em>tableid</em>: курсор, расположенный на записи, для которой извлекается значение по умолчанию, определенное пользователем.</span><span class="sxs-lookup"><span data-stu-id="31447-210"><em>tableid</em>: A cursor positioned on the record for which the user defined default value is being retrieved</span></span></p></li>
<li><p><span data-ttu-id="31447-211"><em>pvArg1</em>: выходной буфер для определяемого пользователем значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="31447-211"><em>pvArg1</em>: The output buffer for the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="31447-212"><em>pvArg2</em>: на входе — это размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="31447-212"><em>pvArg2</em>: On input, this is the size of the output buffer.</span></span> <span data-ttu-id="31447-213">На выходе это фактический размер определяемого пользователем значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31447-213">On output, this is the actual size of the user defined default value.</span></span> <span data-ttu-id="31447-214">в любом случае размер — это 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="31447-214">in either case, the size is a 32-bit unsigned integer.</span></span></p></li>
<li><p><span data-ttu-id="31447-215"><em>пвконтекст</em>: указатель на буфер, содержащий пользовательские данные, указанные в структуре <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> при создании столбца, или значение null, если контекст не был предоставлен.</span><span class="sxs-lookup"><span data-stu-id="31447-215"><em>pvContext</em>: A pointer to a buffer containing the user data specified in the <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure when the column was created or NULL if no context was provided.</span></span></p></li>
<li><p><span data-ttu-id="31447-216"><em>улунусед</em>: идентификатор столбца, для которого извлекается значение по умолчанию, определенное пользователем.</span><span class="sxs-lookup"><span data-stu-id="31447-216"><em>ulUnused</em>: The column ID of the column for which the user defined default value is being retrieved.</span></span></p></li>
</ul>
<p><span data-ttu-id="31447-217">Если функция обратного вызова возвращает ошибку, то операция, исходящий обратный вызов, завершится с такой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="31447-217">If an error is returned by the callback then the operation originating the callback will fail with that error.</span></span></p>
<p><span data-ttu-id="31447-218">Если функция обратного вызова возвращает JET_wrnBufferTruncated, операция продолжится, но во время обратного вызова не будет получено все значение.</span><span class="sxs-lookup"><span data-stu-id="31447-218">If JET_wrnBufferTruncated is returned by the callback, the operation will continue, but the entire value is not retrieved during the callback.</span></span></p>
<p><span data-ttu-id="31447-219">Если функция обратного вызова возвращает JET_wrnColumnNull, операция будет продолжена, но определенное пользователем значение по умолчанию для столбца будет равно NULL.</span><span class="sxs-lookup"><span data-stu-id="31447-219">If JET_wrnColumnNull is returned by the callback, the operation will continue, but the user defined default value for the column is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-220">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="31447-220">JET_cbtypOnlineDefragCompleted</span></span><br />
<span data-ttu-id="31447-221">0x00000100</span><span class="sxs-lookup"><span data-stu-id="31447-221">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="31447-222">Этот обратный вызов происходит, когда оперативная дефрагментация базы данных, инициированной <a href="gg269317(v=exchg.10).md">жетдефрагмент</a> , была остановлена из-за завершения процесса или превышения предельного значения времени.</span><span class="sxs-lookup"><span data-stu-id="31447-222">This callback will occur when the online defragmentation of a database as initiated by <a href="gg269317(v=exchg.10).md">JetDefragment</a> has stopped due to either the process being completed or the time limit being reached.</span></span></p>
<p><span data-ttu-id="31447-223">Указатель на функцию для этой причины обратного вызова передается в <a href="gg269317(v=exchg.10).md">жетдефрагмент</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-223">The function pointer for this callback reason is passed to <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span> <span data-ttu-id="31447-224">Дополнительные сведения см. в разделе <a href="gg269317(v=exchg.10).md">жетдефрагмент</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-224">For more information, see <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span></p>
<p><span data-ttu-id="31447-225">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-225">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-226"><em>сесид</em>: сеанс, используемый для выполнения оперативной дефрагментации базы данных или JET_sesidNil для потокового файла.</span><span class="sxs-lookup"><span data-stu-id="31447-226"><em>sesid</em>: The session used to perform online defragmentation for the database or JET_sesidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="31447-227"><em>DBID</em>: идентификатор базы данных, дефрагментированной или JET_dbidNil для потокового файла.</span><span class="sxs-lookup"><span data-stu-id="31447-227"><em>dbid</em>: The database ID of the database being defragmented or JET_dbidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="31447-228"><em>tableid</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="31447-228"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-229"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-229"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-230"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-230"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-231"><em>пвконтекст</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-231"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-232"><em>улунусед</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-232"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="31447-233">Если обратный вызов возвращает ошибку, она будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="31447-233">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31447-234">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="31447-234">JET_cbtypFreeCursorLS</span></span><br />
<span data-ttu-id="31447-235">0x00000200</span><span class="sxs-lookup"><span data-stu-id="31447-235">0x00000200</span></span></p></td>
<td><p><span data-ttu-id="31447-236">Этот обратный вызов происходит, когда приложению необходимо очистить контекстный обработчик для локального хранилища, связанного с курсором, который освобождается ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="31447-236">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="31447-237">Дополнительные сведения см. в разделе <a href="gg269243(v=exchg.10).md">жетсетлс</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-237">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="31447-238">Указатель на функцию для этой причины обратного вызова настроен с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-238">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-239">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-239">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-240"><em>сесид</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="31447-240"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-241"><em>DBID</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="31447-241"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-242"><em>tableid</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="31447-242"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-243"><em>pvArg1</em>: набор маркеров контекста с помощью <a href="gg269243(v=exchg.10).md">жетсетлс</a></span><span class="sxs-lookup"><span data-stu-id="31447-243"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a></span></span></p></li>
<li><p><span data-ttu-id="31447-244"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-244"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-245"><em>пвконтекст</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-245"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-246"><em>улунусед</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-246"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="31447-247">Если обратный вызов возвращает ошибку, она будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="31447-247">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-248">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="31447-248">JET_cbtypFreeTableLS</span></span><br />
<span data-ttu-id="31447-249">0x00000400</span><span class="sxs-lookup"><span data-stu-id="31447-249">0x00000400</span></span></p></td>
<td><p><span data-ttu-id="31447-250">Этот обратный вызов будет выполняться в результате необходимости в приложении очистить контекстный обработчик для локального хранилища, связанного с таблицей, которая освобождается ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="31447-250">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="31447-251">Дополнительные сведения см. в разделе <a href="gg269243(v=exchg.10).md">жетсетлс</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-251">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="31447-252">Указатель на функцию для этой причины обратного вызова настроен с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-252">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="31447-253">Параметры обратного вызова будут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="31447-253">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31447-254"><em>сесид</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="31447-254"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-255"><em>DBID</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="31447-255"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-256"><em>tableid</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="31447-256"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="31447-257"><em>pvArg1</em>: набор маркеров контекста с помощью <a href="gg269243(v=exchg.10).md">жетсетлс</a>.</span><span class="sxs-lookup"><span data-stu-id="31447-257"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p></li>
<li><p><span data-ttu-id="31447-258"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-258"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-259"><em>пвконтекст</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-259"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="31447-260"><em>улунусед</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="31447-260"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="31447-261">Если обратный вызов возвращает ошибку, она будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="31447-261">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="31447-262">Требования</span><span class="sxs-lookup"><span data-stu-id="31447-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31447-263"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="31447-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="31447-264">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31447-264">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31447-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="31447-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="31447-266">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="31447-266">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31447-267"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="31447-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="31447-268">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="31447-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="31447-269">См. также:</span><span class="sxs-lookup"><span data-stu-id="31447-269">See Also</span></span>

[<span data-ttu-id="31447-270">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="31447-270">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)

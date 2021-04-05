---
description: Дополнительные сведения о функции Жетжетинстанцеинфо
title: Функция Жетжетинстанцеинфо
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911443"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="47930-103">Функция Жетжетинстанцеинфо</span><span class="sxs-lookup"><span data-stu-id="47930-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="47930-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="47930-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="47930-105">Функция Жетжетинстанцеинфо</span><span class="sxs-lookup"><span data-stu-id="47930-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="47930-106">Функция **жетжетинстанцеинфо** извлекает сведения о выполняемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="47930-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="47930-107">**Windows XP: жетжетинстанцеинфо** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47930-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="47930-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47930-108">Parameters</span></span>

<span data-ttu-id="47930-109">*пЦинстанцеинфо*</span><span class="sxs-lookup"><span data-stu-id="47930-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="47930-110">Указатель на буфер, который получит количество элементов, хранящихся в *паинстанцеинфо*.</span><span class="sxs-lookup"><span data-stu-id="47930-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="47930-111">*паинстанцеинфо*</span><span class="sxs-lookup"><span data-stu-id="47930-111">*paInstanceInfo*</span></span>

<span data-ttu-id="47930-112">Указатель на буфер, который получит адрес первого элемента массива структур.</span><span class="sxs-lookup"><span data-stu-id="47930-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="47930-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47930-113">Return Value</span></span>

<span data-ttu-id="47930-114">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="47930-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="47930-115">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="47930-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47930-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="47930-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="47930-117">Описание</span><span class="sxs-lookup"><span data-stu-id="47930-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47930-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="47930-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="47930-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="47930-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47930-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="47930-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="47930-121">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="47930-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="47930-122">Эта ошибка будет возвращена <strong>жетжетинстанцеинфо</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="47930-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="47930-123"><em>пЦинстанцеинфо</em> или <em>паинстанцеинфо</em> имеют значение null.</span><span class="sxs-lookup"><span data-stu-id="47930-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47930-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="47930-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="47930-125">Недостаточно памяти для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="47930-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="47930-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47930-126">Remarks</span></span>

<span data-ttu-id="47930-127">Ядро СУБД выделит массив структур [JET_INSTANCE_INFO](./jet-instance-info-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="47930-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="47930-128">Вызывающий объект отвечает за освобождение этой памяти с помощью [жетфрибуффер](./jetfreebuffer-function.md).</span><span class="sxs-lookup"><span data-stu-id="47930-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="47930-129">Если активных экземпляров нет, **жетжетинстанцеинфо** возвратит JET_errSuccess, а *пЦинстанцеинфо* получит значение 0.</span><span class="sxs-lookup"><span data-stu-id="47930-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="47930-130">Требования</span><span class="sxs-lookup"><span data-stu-id="47930-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47930-131"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="47930-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="47930-132">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47930-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47930-133"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="47930-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="47930-134">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="47930-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47930-135"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="47930-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="47930-136">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="47930-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47930-137"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="47930-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="47930-138">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="47930-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47930-139"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="47930-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="47930-140">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="47930-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47930-141"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="47930-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="47930-142">Реализуется как <strong>жетжетинстанцеинфов</strong> (Юникод) и <strong>жетжетинстанцеинфоа</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="47930-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="47930-143">См. также:</span><span class="sxs-lookup"><span data-stu-id="47930-143">See Also</span></span>

[<span data-ttu-id="47930-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="47930-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="47930-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="47930-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="47930-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="47930-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="47930-147">жетфрибуффер</span><span class="sxs-lookup"><span data-stu-id="47930-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)

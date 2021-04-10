---
description: Дополнительные сведения о функции ЖетжетинстанцемисЦинфо
title: Функция ЖетжетинстанцемисЦинфо
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081180"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="15f05-103">Функция ЖетжетинстанцемисЦинфо</span><span class="sxs-lookup"><span data-stu-id="15f05-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="15f05-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="15f05-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="15f05-105">Функция ЖетжетинстанцемисЦинфо</span><span class="sxs-lookup"><span data-stu-id="15f05-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="15f05-106">Функция **жетжетинстанцемисЦинфо** получает сведения об экземпляре, в то время как экземпляр находится в режиме «в сети».</span><span class="sxs-lookup"><span data-stu-id="15f05-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="15f05-107">**Windows Vista: жетжетинстанцемисЦинфо** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15f05-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="15f05-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15f05-108">Parameters</span></span>

<span data-ttu-id="15f05-109">*вхождение*</span><span class="sxs-lookup"><span data-stu-id="15f05-109">*instance*</span></span>

<span data-ttu-id="15f05-110">Определяет экземпляр базы данных, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="15f05-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="15f05-111">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="15f05-111">*pvResult*</span></span>

<span data-ttu-id="15f05-112">Указатель на буфер, который будет принимать сведения.</span><span class="sxs-lookup"><span data-stu-id="15f05-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="15f05-113">Тип буфера зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="15f05-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="15f05-114">Вызывающий объект отвечает за правильное согласование буфера.</span><span class="sxs-lookup"><span data-stu-id="15f05-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="15f05-115">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="15f05-115">*cbMax*</span></span>

<span data-ttu-id="15f05-116">Размер буфера (в байтах), переданного в *пвресулт*.</span><span class="sxs-lookup"><span data-stu-id="15f05-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="15f05-117">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="15f05-117">*InfoLevel*</span></span>

<span data-ttu-id="15f05-118">Определяет, какой тип данных будет извлечен для экземпляра, заданного *экземпляром*.</span><span class="sxs-lookup"><span data-stu-id="15f05-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="15f05-119">Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="15f05-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="15f05-120">Для использования с этим параметром доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="15f05-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15f05-121">Значение</span><span class="sxs-lookup"><span data-stu-id="15f05-121">Value</span></span></p></th>
<th><p><span data-ttu-id="15f05-122">Значение</span><span class="sxs-lookup"><span data-stu-id="15f05-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15f05-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="15f05-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="15f05-124"><em>пвресулт</em> интерпретируется как структура <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> последовательности журнала транзакций, связанной с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="15f05-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="15f05-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15f05-125">Return Value</span></span>

<span data-ttu-id="15f05-126">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="15f05-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="15f05-127">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="15f05-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15f05-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="15f05-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="15f05-129">Описание</span><span class="sxs-lookup"><span data-stu-id="15f05-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15f05-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="15f05-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="15f05-131">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="15f05-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15f05-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="15f05-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="15f05-133">Буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="15f05-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15f05-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="15f05-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="15f05-135">Указан недопустимый <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> или недопустимое значение <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="15f05-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="15f05-136">Требования</span><span class="sxs-lookup"><span data-stu-id="15f05-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15f05-137"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="15f05-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="15f05-138">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15f05-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15f05-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="15f05-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="15f05-140">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="15f05-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15f05-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="15f05-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="15f05-142">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="15f05-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15f05-143"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="15f05-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="15f05-144">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="15f05-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15f05-145"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="15f05-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="15f05-146">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="15f05-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="15f05-147">См. также:</span><span class="sxs-lookup"><span data-stu-id="15f05-147">See Also</span></span>

[<span data-ttu-id="15f05-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="15f05-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="15f05-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="15f05-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="15f05-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="15f05-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)

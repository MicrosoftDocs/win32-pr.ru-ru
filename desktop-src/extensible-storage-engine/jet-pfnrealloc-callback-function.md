---
description: 'Дополнительные сведения: функция обратного вызова JET_PFNREALLOC'
title: Функция обратного вызова JET_PFNREALLOC
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272858"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="da684-103">Функция обратного вызова JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="da684-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="da684-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="da684-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="da684-105">Функция обратного вызова JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="da684-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="da684-106">Функция JET_PFNREALLOC представляет [собой совместимый с](/cpp/c-runtime-library/reference/realloc?view=vs-2019) перераспределением обратный вызов, используемый [жетенумератеколумнс](./jetenumeratecolumns-function.md) для выделения памяти для буферов вывода.</span><span class="sxs-lookup"><span data-stu-id="da684-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="da684-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="da684-107">Parameters</span></span>

<span data-ttu-id="da684-108">*пвконтекст*</span><span class="sxs-lookup"><span data-stu-id="da684-108">*pvContext*</span></span>

<span data-ttu-id="da684-109">Указатель контекста, переданный в [жетенумератеколумнс](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="da684-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="da684-110">Этот указатель контекста можно использовать для передачи состояния из вызывающего объекта [жетенумератеколумнс](./jetenumeratecolumns-function.md) в реализацию этого обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="da684-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="da684-111">*PV*</span><span class="sxs-lookup"><span data-stu-id="da684-111">*pv*</span></span>

<span data-ttu-id="da684-112">Если значение не равно NULL, указывает указатель на блок памяти, ранее выделенный этим обратным вызовом.</span><span class="sxs-lookup"><span data-stu-id="da684-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="da684-113">Если значение равно NULL, выделяется новый блок памяти запрошенного размера.</span><span class="sxs-lookup"><span data-stu-id="da684-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="da684-114">*CB*</span><span class="sxs-lookup"><span data-stu-id="da684-114">*cb*</span></span>

<span data-ttu-id="da684-115">Новый размер блока памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="da684-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="da684-116">Если этот параметр имеет значение 0 (ноль) и указан блок памяти, то этот блок памяти будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="da684-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="da684-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da684-117">Return Value</span></span>

<span data-ttu-id="da684-118">Система может создать коды успеха или сбоя в результате вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="da684-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="da684-119">Сведения о том, как вернуть эти коды HRESULT, см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="da684-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da684-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="da684-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="da684-121">Описание</span><span class="sxs-lookup"><span data-stu-id="da684-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da684-122">Успешно</span><span class="sxs-lookup"><span data-stu-id="da684-122">Success</span></span></p></td>
<td><p><span data-ttu-id="da684-123">Если был указан ранее выделенный блок памяти и был указан новый нулевой размер, этот блок освобождается и возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="da684-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="da684-124">Если был указан ранее выделенный блок памяти и не был указан ненулевой размер, возвращается блок памяти с перераспределением.</span><span class="sxs-lookup"><span data-stu-id="da684-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="da684-125">Если блок памяти не указан, возвращается только что выделенный блок памяти указанного размера.</span><span class="sxs-lookup"><span data-stu-id="da684-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da684-126">Failure</span><span class="sxs-lookup"><span data-stu-id="da684-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="da684-127">Будет возвращено значение NULL.</span><span class="sxs-lookup"><span data-stu-id="da684-127">NULL will be returned.</span></span> <span data-ttu-id="da684-128">Если был предоставлен ранее выделенный блок памяти, этот блок останется выделенным.</span><span class="sxs-lookup"><span data-stu-id="da684-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="da684-129">Требования</span><span class="sxs-lookup"><span data-stu-id="da684-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da684-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="da684-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="da684-131">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="da684-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da684-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="da684-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="da684-133">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="da684-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da684-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="da684-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="da684-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="da684-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="da684-136">См. также:</span><span class="sxs-lookup"><span data-stu-id="da684-136">See Also</span></span>

[<span data-ttu-id="da684-137">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="da684-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

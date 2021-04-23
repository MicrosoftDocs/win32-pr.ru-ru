---
description: Дополнительные сведения о функции Жетжетсессионпараметер
title: Функция Жетжетсессионпараметер
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896701"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="25209-103">Функция Жетжетсессионпараметер</span><span class="sxs-lookup"><span data-stu-id="25209-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="25209-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25209-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="25209-105">Функция **жетжетсессионпараметер** считывает параметр сеанса для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="25209-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="25209-106">Функция **жетжетсессионпараметер** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25209-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="25209-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="25209-107">Parameters</span></span>

<span data-ttu-id="25209-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="25209-108">*sesid*</span></span>

<span data-ttu-id="25209-109">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="25209-109">The session to use for this call.</span></span>

<span data-ttu-id="25209-110">Если этот параметр указан, то указанный экземпляр игнорируется, и будет использоваться экземпляр, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="25209-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="25209-111">*сеспарамид*</span><span class="sxs-lookup"><span data-stu-id="25209-111">*sesparamid*</span></span>

<span data-ttu-id="25209-112">ИДЕНТИФИКАТОР устанавливаемого параметра сеанса.</span><span class="sxs-lookup"><span data-stu-id="25209-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="25209-113">*пвпарам*</span><span class="sxs-lookup"><span data-stu-id="25209-113">*pvParam*</span></span>

<span data-ttu-id="25209-114">Данные в этом параметре сеанса.</span><span class="sxs-lookup"><span data-stu-id="25209-114">Data in this session parameter.</span></span>

<span data-ttu-id="25209-115">*кбпараммакс*</span><span class="sxs-lookup"><span data-stu-id="25209-115">*cbParamMax*</span></span>

<span data-ttu-id="25209-116">Максимальный размер набора данных в этом параметре сеанса.</span><span class="sxs-lookup"><span data-stu-id="25209-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="25209-117">*пкбпарамактуал*</span><span class="sxs-lookup"><span data-stu-id="25209-117">*pcbParamActual*</span></span>

<span data-ttu-id="25209-118">Фактический размер набора данных в этом параметре сеанса.</span><span class="sxs-lookup"><span data-stu-id="25209-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="25209-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25209-119">Return value</span></span>

<span data-ttu-id="25209-120">В случае успеха выходной буфер, соответствующий запрошенному параметру сеанса, будет установлен в значение этого параметра сеанса.</span><span class="sxs-lookup"><span data-stu-id="25209-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="25209-121">В случае сбоя состояние выходных буферов будет не определено.</span><span class="sxs-lookup"><span data-stu-id="25209-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="25209-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25209-122">Remarks</span></span>

<span data-ttu-id="25209-123">Параметр Session используется в течение времени существования сеанса или до тех пор, пока значение не будет сброшено.</span><span class="sxs-lookup"><span data-stu-id="25209-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="25209-124">Требования</span><span class="sxs-lookup"><span data-stu-id="25209-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25209-125"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="25209-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="25209-126">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25209-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25209-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="25209-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="25209-128">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="25209-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25209-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="25209-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="25209-130">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="25209-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25209-131"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="25209-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="25209-132">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="25209-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25209-133"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="25209-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="25209-134">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="25209-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="25209-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25209-135">See also</span></span>

[<span data-ttu-id="25209-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="25209-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="25209-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="25209-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="25209-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="25209-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="25209-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="25209-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="25209-140">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="25209-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="25209-141">жетинит</span><span class="sxs-lookup"><span data-stu-id="25209-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="25209-142">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="25209-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="25209-143">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="25209-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="25209-144">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="25209-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

---
title: Метод Иделиверйоптимизатионжоб Аддфилевисранжес (Deliveryoptimization. h)
description: Добавляет файл в задание загрузки и задает диапазоны файлов, которые необходимо загрузить.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Метод Аддфилевисранжес
- Метод Аддфилевисранжес, интерфейс Иделиверйоптимизатионжоб
- Интерфейс Иделиверйоптимизатионжоб, метод Аддфилевисранжес
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710551"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="c4406-106">Метод Иделиверйоптимизатионжоб:: Аддфилевисранжес</span><span class="sxs-lookup"><span data-stu-id="c4406-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="c4406-107">Добавляет файл в задание загрузки и задает диапазоны файлов, которые необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="c4406-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4406-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4406-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="c4406-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4406-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4406-110">*ИД* \[ для окне\]</span><span class="sxs-lookup"><span data-stu-id="c4406-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4406-111">Строка, заканчивающаяся нулем, которая является уникальным идентификатором опубликованного содержимого.</span><span class="sxs-lookup"><span data-stu-id="c4406-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="c4406-112">Для неопубликованного содержимого это может быть любая уникальная строка, которую вызывающий объект может использовать для идентификации файлов в задании.</span><span class="sxs-lookup"><span data-stu-id="c4406-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="c4406-113">*ремотеурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4406-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4406-114">Строка, заканчивающаяся нулем и содержащая имя файла на сервере.</span><span class="sxs-lookup"><span data-stu-id="c4406-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="c4406-115">*LocalName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4406-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4406-116">Строка, заканчивающаяся нулем и содержащая имя файла на клиенте.</span><span class="sxs-lookup"><span data-stu-id="c4406-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="c4406-117">*ранжекаунт* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c4406-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4406-118">Число элементов в *диапазонах*.</span><span class="sxs-lookup"><span data-stu-id="c4406-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="c4406-119">*диапазоны* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c4406-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4406-120">Массив из одной или нескольких структур [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) , указывающих диапазоны для загрузки.</span><span class="sxs-lookup"><span data-stu-id="c4406-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="c4406-121">Не указывайте дублирующиеся или перекрывающиеся диапазоны.</span><span class="sxs-lookup"><span data-stu-id="c4406-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="c4406-122">*Размер файла* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c4406-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4406-123">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="c4406-123">Size of the file in bytes.</span></span> <span data-ttu-id="c4406-124">Передайте **DO_UNKNOWN_FILE_SIZE** , если размер не известен вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="c4406-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4406-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4406-125">Return value</span></span>

<span data-ttu-id="c4406-126">Этот метод возвращает следующие возвращаемые значения, а также другие.</span><span class="sxs-lookup"><span data-stu-id="c4406-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4406-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c4406-127">Return code</span></span></th>
<th><span data-ttu-id="c4406-128">Описание</span><span class="sxs-lookup"><span data-stu-id="c4406-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="c4406-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4406-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c4406-130">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c4406-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c4406-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4406-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c4406-132">Имя локального файла имеет значение NULL или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="c4406-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c4406-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4406-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c4406-134">У пользователя нет разрешения на запись в указанный каталог на клиенте.</span><span class="sxs-lookup"><span data-stu-id="c4406-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c4406-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4406-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c4406-136">Один из диапазонов недопустим.</span><span class="sxs-lookup"><span data-stu-id="c4406-136">One of the ranges is invalid.</span></span> <span data-ttu-id="c4406-137">Например, Инитиалоффсет имеет значение <strong>BG_LENGTH_TO_EOF</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4406-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c4406-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4406-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c4406-139">Нельзя указывать дублирующиеся или перекрывающиеся диапазоны.</span><span class="sxs-lookup"><span data-stu-id="c4406-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c4406-140">Диапазоны сортируются по смещению значения, а не к длине.</span><span class="sxs-lookup"><span data-stu-id="c4406-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="c4406-141">Если введены диапазоны с одинаковым смещением, но находятся в обратном порядке, возвращается эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="c4406-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="c4406-142">Например, если в этом порядке введены 100,5 и 100,0, вы не сможете добавить файл в задание.</span><span class="sxs-lookup"><span data-stu-id="c4406-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c4406-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c4406-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c4406-144">Состояние задания не может быть <strong>BG_JOB_STATE_CANCELLED</strong> или <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4406-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c4406-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c4406-145">Requirements</span></span>



| <span data-ttu-id="c4406-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c4406-146">Requirement</span></span> | <span data-ttu-id="c4406-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c4406-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4406-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4406-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c4406-149">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c4406-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4406-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4406-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c4406-151">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c4406-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c4406-152">Header</span><span class="sxs-lookup"><span data-stu-id="c4406-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4406-153"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4406-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4406-154">IDL</span><span class="sxs-lookup"><span data-stu-id="c4406-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4406-155"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4406-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4406-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4406-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4406-157"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4406-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c4406-158">DLL</span><span class="sxs-lookup"><span data-stu-id="c4406-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4406-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4406-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c4406-160">IID</span><span class="sxs-lookup"><span data-stu-id="c4406-160">IID</span></span><br/>                      | <span data-ttu-id="c4406-161">IID_IDeliveryOptimizationJob определяется как EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="c4406-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c4406-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4406-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4406-163">**иделиверйоптимизатионжоб**</span><span class="sxs-lookup"><span data-stu-id="c4406-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 


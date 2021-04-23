---
description: Дополнительные сведения о функции Жетжетерроринфов
title: Функция Жетжетерроринфов
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157282"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="d84df-103">Функция Жетжетерроринфов</span><span class="sxs-lookup"><span data-stu-id="d84df-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="d84df-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d84df-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="d84df-105">Функция Жетжетерроринфов</span><span class="sxs-lookup"><span data-stu-id="d84df-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="d84df-106">Функция **жетжетерроринфов** BAS_ ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="d84df-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="d84df-107">Примечание. Эта документация основана на предварительном выпуске расширяемой подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="d84df-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="d84df-108">Эта информация может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="d84df-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="d84df-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d84df-109">Parameters</span></span>

<span data-ttu-id="d84df-110">*пвконтекст*</span><span class="sxs-lookup"><span data-stu-id="d84df-110">*pvContext*</span></span>

<span data-ttu-id="d84df-111">Контекст или значение ошибки, для которого требуются расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d84df-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="d84df-112">Передаваемое значение зависит от значения параметра *инфолевел* .</span><span class="sxs-lookup"><span data-stu-id="d84df-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="d84df-113">*пвресулт*</span><span class="sxs-lookup"><span data-stu-id="d84df-113">*pvResult*</span></span>

<span data-ttu-id="d84df-114">Указатель на буфер, который будет принимать сведения.</span><span class="sxs-lookup"><span data-stu-id="d84df-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="d84df-115">Тип буфера зависит от значения параметра *инфолевел* .</span><span class="sxs-lookup"><span data-stu-id="d84df-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="d84df-116">Вызывающий объект должен быть настроен для правильного согласования буфера.</span><span class="sxs-lookup"><span data-stu-id="d84df-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="d84df-117">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="d84df-117">*cbMax*</span></span>

<span data-ttu-id="d84df-118">Максимальный размер передаваемой структуры *пвресулт* .</span><span class="sxs-lookup"><span data-stu-id="d84df-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="d84df-119">*инфолевел*</span><span class="sxs-lookup"><span data-stu-id="d84df-119">*InfoLevel*</span></span>

<span data-ttu-id="d84df-120">Тип сведений, которые будут получены для сведений об ошибке или контекста, задается параметром *пвконтекст* .</span><span class="sxs-lookup"><span data-stu-id="d84df-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="d84df-121">Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.</span><span class="sxs-lookup"><span data-stu-id="d84df-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="d84df-122">В следующей таблице перечислены возможные значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="d84df-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d84df-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d84df-123">Value</span></span></p></th>
<th><p><span data-ttu-id="d84df-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d84df-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d84df-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="d84df-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="d84df-126"><em>пвконтекст</em> интерпретируется как код/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>пвресулт</em> интерпретируется как <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, а поля структуры <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> заполняются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d84df-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d84df-127">*грбит*</span><span class="sxs-lookup"><span data-stu-id="d84df-127">*grbit*</span></span>

<span data-ttu-id="d84df-128">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d84df-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="d84df-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d84df-129">Return Value</span></span>

<span data-ttu-id="d84df-130">Эта функция возвращает [JET_ERR](./extensible-storage-engine-error-codes.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d84df-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="d84df-131">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d84df-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d84df-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d84df-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="d84df-133">Описание</span><span class="sxs-lookup"><span data-stu-id="d84df-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d84df-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d84df-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d84df-135">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d84df-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d84df-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d84df-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d84df-137">Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</span><span class="sxs-lookup"><span data-stu-id="d84df-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="d84df-138">Это может произойти для <strong>жетжетерроринфо</strong> , когда происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="d84df-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="d84df-139">Указано недопустимое значение параметра <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="d84df-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="d84df-140">Указано недопустимое значение <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="d84df-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="d84df-141">Указанное значение <em>кбмакс</em> буфера параметра <em>пвресулт</em> меньше, чем требуемый размер для выходных данных этого параметра <em>инфолевел</em> .</span><span class="sxs-lookup"><span data-stu-id="d84df-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="d84df-142">Для <em>инфолевел</em> = JET_ErrorInfoSpecificErr переданное значение <a href="gg294092(v=exchg.10).md">JET_ERR</a> неизвестно подсистеме.</span><span class="sxs-lookup"><span data-stu-id="d84df-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d84df-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="d84df-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="d84df-144">Если этот номер SKU Windows не поддерживает эту функцию, будет возвращена эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="d84df-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d84df-145">При успешном завершении для выходного буфера, соответствующего запрошенному контексту или значению ошибки, будут установлены запрошенные расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d84df-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="d84df-146">В случае сбоя состояние выходных буферов будет не определено.</span><span class="sxs-lookup"><span data-stu-id="d84df-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="d84df-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d84df-147">Remarks</span></span>

<span data-ttu-id="d84df-148">Функция [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) и [JET_ERRCAT](./jet-errcat.md) группы констант содержат документацию о расширенных сведениях об ошибках, возвращаемых для *инфолевел* = JET_ErrorInfoSpecificErr.</span><span class="sxs-lookup"><span data-stu-id="d84df-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="d84df-149">Требования</span><span class="sxs-lookup"><span data-stu-id="d84df-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d84df-150"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d84df-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d84df-151">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d84df-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d84df-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d84df-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d84df-153">Требуется Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="d84df-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d84df-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d84df-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d84df-155">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d84df-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d84df-156"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="d84df-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d84df-157">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d84df-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d84df-158"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="d84df-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d84df-159">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d84df-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d84df-160"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="d84df-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d84df-161">Примечание. реализуется только <strong>жетжетерроринфов</strong> (Unicode).</span><span class="sxs-lookup"><span data-stu-id="d84df-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="d84df-162">Этот API не имеет версию A (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d84df-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>

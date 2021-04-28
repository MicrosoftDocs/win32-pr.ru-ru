---
description: 'Метод Истатс:: Connect. метод Connect подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации для подключения.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'Метод Истатс:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098482"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="6949a-103">Метод Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="6949a-103">IStats::Connect method</span></span>

<span data-ttu-id="6949a-104">Метод **Connect** подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации для подключения.</span><span class="sxs-lookup"><span data-stu-id="6949a-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6949a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6949a-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6949a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6949a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6949a-107">*хинпутблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6949a-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6949a-108">Обработчик для большого двоичного объекта, указывающий сетевую карту, к которой подключается НПП, и сведения о конфигурации для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="6949a-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="6949a-109">*Статускаллбаккпрок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6949a-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6949a-110">Адрес функции обратного вызова пользователя, которая получает обновления состояния, такие как триггеры.</span><span class="sxs-lookup"><span data-stu-id="6949a-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="6949a-111">Если функция обратного вызова не используется, присвойте этому параметру и параметру *UserContext* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6949a-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6949a-112">*UserContext* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6949a-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6949a-113">Значение, передаваемое при вызове функции обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="6949a-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="6949a-114">Значением этого параметра обычно является HWND или указатель this.</span><span class="sxs-lookup"><span data-stu-id="6949a-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="6949a-115">Если функция обратного вызова не указана, присвойте этому параметру и параметру *Статускаллбаккпрок* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6949a-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6949a-116">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6949a-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6949a-117">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6949a-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6949a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6949a-118">Return value</span></span>

<span data-ttu-id="6949a-119">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6949a-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6949a-120">Если метод завершился неудачно, возвращаемое значение является одним из следующих кодов ошибок (которые содержат ошибки, возвращенные внутренним вызовом **истатс:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="6949a-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6949a-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6949a-121">Return code</span></span></th>
<th><span data-ttu-id="6949a-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6949a-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="6949a-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-124">Этот экземпляр COM-объекта НПП уже подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="6949a-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6949a-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-126">Большой двоичный объект конфигурации поврежден.</span><span class="sxs-lookup"><span data-stu-id="6949a-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="6949a-127">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6949a-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-129">Входной большой двоичный объект, заданный параметром <em>хинпутблоб</em> , не имеет записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="6949a-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="6949a-130">Эта ошибка может быть вызвана вызовом <strong>истатс:: Connect</strong> или <strong>Истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="6949a-131">Посмотрите на большой двоичный объект Error, возвращенный <em>херрорблоб</em> , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="6949a-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6949a-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-133">Функция <strong>CreateBlob</strong> не была вызвана.</span><span class="sxs-lookup"><span data-stu-id="6949a-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="6949a-134">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6949a-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-136">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="6949a-136">The string is not null-terminated.</span></span> <span data-ttu-id="6949a-137">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6949a-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-139">Часть триггера входного большого двоичного объекта повреждена.</span><span class="sxs-lookup"><span data-stu-id="6949a-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="6949a-140">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6949a-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-142">Объект, указанный в <em>хинпутблоб</em> , не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="6949a-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="6949a-143">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6949a-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-145">Каталог записи по умолчанию не был задан в реестре.</span><span class="sxs-lookup"><span data-stu-id="6949a-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="6949a-146">Чтобы задать каталог записи, используйте следующий путь.</span><span class="sxs-lookup"><span data-stu-id="6949a-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6949a-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-148">Объем памяти, необходимый для выполнения этой операции, недоступен.</span><span class="sxs-lookup"><span data-stu-id="6949a-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="6949a-149">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6949a-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-151">Время ожидания запроса истекло. Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6949a-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6949a-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6949a-153">Неверный номер версии большого двоичного объекта, указанного в <em>хинпутблоб</em> .</span><span class="sxs-lookup"><span data-stu-id="6949a-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="6949a-154">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="6949a-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6949a-155">Remarks</span><span class="sxs-lookup"><span data-stu-id="6949a-155">Remarks</span></span>

<span data-ttu-id="6949a-156">При вызове метода **Connect** сетевой монитор автоматически вызывает метод **Истатс:: Configure** с помощью большого двоичного объекта, предоставленного параметром *хинпутблоб* .</span><span class="sxs-lookup"><span data-stu-id="6949a-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="6949a-157">Обратите внимание, что все коды ошибок, возвращенные вызовом **истатс:: Configure** , передаются обратно и возвращаются вызовом **Истатс:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="6949a-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="6949a-158">Этот метод должен быть вызван до начала записи кадров.</span><span class="sxs-lookup"><span data-stu-id="6949a-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="6949a-159">Обратите внимание, что при подключении к сети с помощью этого метода необходимо продолжить использовать интерфейс **истатс** для записи кадров.</span><span class="sxs-lookup"><span data-stu-id="6949a-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="6949a-160">Входной большой двоичный объект, заданный параметром *хинпутблоб* , можно получить, вызвав методы **жетнппблобфромуи**, **жетнппблобтабле** и **селектнппблобфромтабле** .</span><span class="sxs-lookup"><span data-stu-id="6949a-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="6949a-161">BLOB-объект ошибки, возвращенный параметром *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти во входном большом двоичном объекте, указанном в *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="6949a-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="6949a-162">Возвращенный BLOB-объект ошибки содержит сведения об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="6949a-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="6949a-163">Например, если НМЕРР \_ запись BLOB \_ \_ -объекта \_ не \_ существует, запись, которую сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="6949a-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="6949a-164">Сведения о</span><span class="sxs-lookup"><span data-stu-id="6949a-164">For information about</span></span>                                             | <span data-ttu-id="6949a-165">См.</span><span class="sxs-lookup"><span data-stu-id="6949a-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6949a-166">Получение входного большого двоичного объекта, представляющего сетевую карту</span><span class="sxs-lookup"><span data-stu-id="6949a-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="6949a-167">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="6949a-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="6949a-168">Требования</span><span class="sxs-lookup"><span data-stu-id="6949a-168">Requirements</span></span>



| <span data-ttu-id="6949a-169">Требование</span><span class="sxs-lookup"><span data-stu-id="6949a-169">Requirement</span></span> | <span data-ttu-id="6949a-170">Значение</span><span class="sxs-lookup"><span data-stu-id="6949a-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6949a-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6949a-171">Minimum supported client</span></span><br/> | <span data-ttu-id="6949a-172">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6949a-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6949a-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6949a-173">Minimum supported server</span></span><br/> | <span data-ttu-id="6949a-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6949a-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6949a-175">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6949a-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="6949a-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6949a-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6949a-177">DLL</span><span class="sxs-lookup"><span data-stu-id="6949a-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6949a-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6949a-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6949a-179">См. также</span><span class="sxs-lookup"><span data-stu-id="6949a-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6949a-180">истатс</span><span class="sxs-lookup"><span data-stu-id="6949a-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="6949a-181">Истатс:: Configure</span><span class="sxs-lookup"><span data-stu-id="6949a-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="6949a-182">Истатс::D подключение</span><span class="sxs-lookup"><span data-stu-id="6949a-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="6949a-183">сетевой монитор большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="6949a-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 





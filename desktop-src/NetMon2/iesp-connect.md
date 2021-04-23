---
description: Метод Connect подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации подключения.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: 'Метод ИЕСП:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4fc9c88b0eb4671c61f268c5857dceba3dc500f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143771"
---
# <a name="iespconnect-method"></a><span data-ttu-id="8c9d9-103">Метод ИЕСП:: Connect</span><span class="sxs-lookup"><span data-stu-id="8c9d9-103">IESP::Connect method</span></span>

<span data-ttu-id="8c9d9-104">Метод **Connect** подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации подключения.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c9d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c9d9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8c9d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c9d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9d9-107">*хинпутблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c9d9-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9d9-108">Обработчик для большого двоичного объекта, указывающий сетевую карту, к которой подключается НПП, и сведения о конфигурации для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="8c9d9-109">*Статускаллбаккпрок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c9d9-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9d9-110">Адрес функции обратного вызова пользователя, которая получает обновления состояния, такие как триггеры.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="8c9d9-111">Если функция обратного вызова не используется, присвойте этому параметру и параметру *UserContext* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8c9d9-112">*UserContext* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c9d9-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9d9-113">Значение, передаваемое при вызове функции обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="8c9d9-114">Значением этого параметра обычно является HWND или указатель this.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="8c9d9-115">Если функция обратного вызова не указана, присвойте этому параметру и параметру *Статускаллбаккпрок* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8c9d9-116">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8c9d9-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9d9-117">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9d9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c9d9-118">Return value</span></span>

<span data-ttu-id="8c9d9-119">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8c9d9-120">Если метод завершился неудачно, возвращаемое значение является одним из следующих кодов ошибок (которые содержат ошибки, возвращенные внутренним вызовом **ИЕСП:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="8c9d9-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IESP::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c9d9-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8c9d9-121">Return code</span></span></th>
<th><span data-ttu-id="8c9d9-122">Описание</span><span class="sxs-lookup"><span data-stu-id="8c9d9-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="8c9d9-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-124">Этот экземпляр COM-объекта НПП уже подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8c9d9-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-126">Большой двоичный объект конфигурации поврежден.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="8c9d9-127">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-127">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8c9d9-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-129">Входной большой двоичный объект, заданный параметром <em>хинпутблоб</em> , не имеет записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="8c9d9-130">Эта ошибка может быть вызвана вызовом <strong>ИЕСП:: Connect</strong> или <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-130">This error might be generated by the <strong>IESP::Connect</strong> or <strong>IESP::Configure</strong> call.</span></span> <span data-ttu-id="8c9d9-131">Посмотрите на большой двоичный объект Error, возвращенный <em>херрорблоб</em> , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8c9d9-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-133">Функция <strong>CreateBlob</strong> не была вызвана.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="8c9d9-134">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-134">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8c9d9-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-136">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-136">The string is not null-terminated.</span></span> <span data-ttu-id="8c9d9-137">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-137">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8c9d9-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-139">Часть триггера входного большого двоичного объекта повреждена.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="8c9d9-140">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-140">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8c9d9-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-142">Объект, указанный в <em>хинпутблоб</em> , не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="8c9d9-143">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-143">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8c9d9-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-145">Каталог записи по умолчанию не был задан в реестре.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="8c9d9-146">Используйте следующий путь, чтобы задать каталог записи.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8c9d9-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-148">Память, необходимая для выполнения этой операции, недоступна.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-148">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="8c9d9-149">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-149">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8c9d9-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-151">Время ожидания запроса истекло. Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-151">The request has timed out. This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8c9d9-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c9d9-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8c9d9-153">Неверный номер версии большого двоичного объекта, указанного в <em>хинпутблоб</em> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="8c9d9-154">Эта ошибка возникает при вызове <strong>ИЕСП:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-154">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8c9d9-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c9d9-155">Remarks</span></span>

<span data-ttu-id="8c9d9-156">При вызове метода **Connect** сетевой монитор автоматически вызывает **ИЕСП:: Configure** с помощью большого двоичного объекта, предоставленного параметром *хинпутблоб* .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-156">When the **Connect** method is called, Network Monitor automatically calls **IESP::Configure** by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="8c9d9-157">Обратите внимание, что все коды ошибок, возвращенные вызовом **ИЕСП:: Configure** , передаются обратно и возвращаются вызовом **ИЕСП:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="8c9d9-157">Note that any error codes returned by the call to **IESP::Configure** are passed back and returned by the **IESP::Connect** call.</span></span>

<span data-ttu-id="8c9d9-158">Этот метод должен быть вызван до начала записи кадров.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="8c9d9-159">Обратите внимание, что при подключении к сети с помощью этого метода необходимо продолжить использовать интерфейс **ИЕСП** для записи кадров.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-159">Note that when you connect to the network by using this method, you must continue to use the **IESP** interface to capture frames.</span></span>

<span data-ttu-id="8c9d9-160">Входной большой двоичный объект, заданный параметром *хинпутблоб* , можно получить, вызвав **жетнппблобфромуи**, **жетнппблобтабле** и **селектнппблобфромтабле**.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-160">The input BLOB specified by *hInputBlob* can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="8c9d9-161">BLOB-объект ошибки, возвращенный *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти во входном большом двоичном объекте, указанном в *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-161">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="8c9d9-162">Возвращенный BLOB-объект ошибки содержит сведения об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="8c9d9-163">Например, если НМЕРР \_ запись BLOB \_ \_ -объекта \_ не \_ существует, запись, которую сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="8c9d9-164">Сведения о</span><span class="sxs-lookup"><span data-stu-id="8c9d9-164">For information about</span></span>                          | <span data-ttu-id="8c9d9-165">См.</span><span class="sxs-lookup"><span data-stu-id="8c9d9-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8c9d9-166">Получение входного большого двоичного объекта, представляющего сетевую карту</span><span class="sxs-lookup"><span data-stu-id="8c9d9-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="8c9d9-167">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="8c9d9-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="8c9d9-168">Требования</span><span class="sxs-lookup"><span data-stu-id="8c9d9-168">Requirements</span></span>



| <span data-ttu-id="8c9d9-169">Требование</span><span class="sxs-lookup"><span data-stu-id="8c9d9-169">Requirement</span></span> | <span data-ttu-id="8c9d9-170">Значение</span><span class="sxs-lookup"><span data-stu-id="8c9d9-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9d9-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c9d9-171">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9d9-172">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c9d9-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8c9d9-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c9d9-173">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9d9-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c9d9-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8c9d9-175">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8c9d9-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9d9-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9d9-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8c9d9-177">DLL</span><span class="sxs-lookup"><span data-stu-id="8c9d9-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c9d9-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c9d9-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9d9-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c9d9-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9d9-180">иесп</span><span class="sxs-lookup"><span data-stu-id="8c9d9-180">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="8c9d9-181">ИЕСП:: Configure</span><span class="sxs-lookup"><span data-stu-id="8c9d9-181">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="8c9d9-182">ИЕСП::D подключение</span><span class="sxs-lookup"><span data-stu-id="8c9d9-182">IESP::Disconnect</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="8c9d9-183">ИЕСП:: Start</span><span class="sxs-lookup"><span data-stu-id="8c9d9-183">IESP::Start</span></span>](iesp-start.md)
</dt> </dl>

 

 





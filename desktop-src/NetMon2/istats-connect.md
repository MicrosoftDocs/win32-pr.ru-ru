---
description: Метод Connect подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации для подключения.
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
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913855"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="934bf-103">Метод Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="934bf-103">IStats::Connect method</span></span>

<span data-ttu-id="934bf-104">Метод **Connect** подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации для подключения.</span><span class="sxs-lookup"><span data-stu-id="934bf-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="934bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="934bf-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="934bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="934bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="934bf-107">*хинпутблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="934bf-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="934bf-108">Обработчик для большого двоичного объекта, указывающий сетевую карту, к которой подключается НПП, и сведения о конфигурации для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="934bf-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="934bf-109">*Статускаллбаккпрок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="934bf-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="934bf-110">Адрес функции обратного вызова пользователя, которая получает обновления состояния, такие как триггеры.</span><span class="sxs-lookup"><span data-stu-id="934bf-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="934bf-111">Если функция обратного вызова не используется, присвойте этому параметру и параметру *UserContext* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="934bf-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="934bf-112">*UserContext* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="934bf-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="934bf-113">Значение, передаваемое при вызове функции обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="934bf-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="934bf-114">Значением этого параметра обычно является HWND или указатель this.</span><span class="sxs-lookup"><span data-stu-id="934bf-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="934bf-115">Если функция обратного вызова не указана, присвойте этому параметру и параметру *Статускаллбаккпрок* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="934bf-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="934bf-116">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="934bf-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="934bf-117">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="934bf-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="934bf-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="934bf-118">Return value</span></span>

<span data-ttu-id="934bf-119">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="934bf-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="934bf-120">Если метод завершился неудачно, возвращаемое значение является одним из следующих кодов ошибок (которые содержат ошибки, возвращенные внутренним вызовом **истатс:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="934bf-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="934bf-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="934bf-121">Return code</span></span></th>
<th><span data-ttu-id="934bf-122">Описание</span><span class="sxs-lookup"><span data-stu-id="934bf-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="934bf-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-124">Этот экземпляр COM-объекта НПП уже подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="934bf-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="934bf-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-126">Большой двоичный объект конфигурации поврежден.</span><span class="sxs-lookup"><span data-stu-id="934bf-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="934bf-127">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="934bf-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-129">Входной большой двоичный объект, заданный параметром <em>хинпутблоб</em> , не имеет записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="934bf-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="934bf-130">Эта ошибка может быть вызвана вызовом <strong>истатс:: Connect</strong> или <strong>Истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="934bf-131">Посмотрите на большой двоичный объект Error, возвращенный <em>херрорблоб</em> , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="934bf-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="934bf-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-133">Функция <strong>CreateBlob</strong> не была вызвана.</span><span class="sxs-lookup"><span data-stu-id="934bf-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="934bf-134">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="934bf-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-136">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="934bf-136">The string is not null-terminated.</span></span> <span data-ttu-id="934bf-137">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="934bf-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-139">Часть триггера входного большого двоичного объекта повреждена.</span><span class="sxs-lookup"><span data-stu-id="934bf-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="934bf-140">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="934bf-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-142">Объект, указанный в <em>хинпутблоб</em> , не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="934bf-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="934bf-143">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="934bf-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-145">Каталог записи по умолчанию не был задан в реестре.</span><span class="sxs-lookup"><span data-stu-id="934bf-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="934bf-146">Чтобы задать каталог записи, используйте следующий путь.</span><span class="sxs-lookup"><span data-stu-id="934bf-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="934bf-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-148">Объем памяти, необходимый для выполнения этой операции, недоступен.</span><span class="sxs-lookup"><span data-stu-id="934bf-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="934bf-149">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="934bf-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-151">Время ожидания запроса истекло. Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="934bf-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="934bf-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="934bf-153">Неверный номер версии большого двоичного объекта, указанного в <em>хинпутблоб</em> .</span><span class="sxs-lookup"><span data-stu-id="934bf-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="934bf-154">Эта ошибка возникает при вызове <strong>истатс:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="934bf-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="934bf-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="934bf-155">Remarks</span></span>

<span data-ttu-id="934bf-156">При вызове метода **Connect** сетевой монитор автоматически вызывает метод **Истатс:: Configure** с помощью большого двоичного объекта, предоставленного параметром *хинпутблоб* .</span><span class="sxs-lookup"><span data-stu-id="934bf-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="934bf-157">Обратите внимание, что все коды ошибок, возвращенные вызовом **истатс:: Configure** , передаются обратно и возвращаются вызовом **Истатс:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="934bf-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="934bf-158">Этот метод должен быть вызван до начала записи кадров.</span><span class="sxs-lookup"><span data-stu-id="934bf-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="934bf-159">Обратите внимание, что при подключении к сети с помощью этого метода необходимо продолжить использовать интерфейс **истатс** для записи кадров.</span><span class="sxs-lookup"><span data-stu-id="934bf-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="934bf-160">Входной большой двоичный объект, заданный параметром *хинпутблоб* , можно получить, вызвав методы **жетнппблобфромуи**, **жетнппблобтабле** и **селектнппблобфромтабле** .</span><span class="sxs-lookup"><span data-stu-id="934bf-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="934bf-161">BLOB-объект ошибки, возвращенный параметром *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти во входном большом двоичном объекте, указанном в *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="934bf-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="934bf-162">Возвращенный BLOB-объект ошибки содержит сведения об ошибке, которые приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="934bf-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="934bf-163">Например, если НМЕРР \_ запись BLOB \_ \_ -объекта \_ не \_ существует, запись, которую сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="934bf-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="934bf-164">Сведения о</span><span class="sxs-lookup"><span data-stu-id="934bf-164">For information about</span></span>                                             | <span data-ttu-id="934bf-165">См.</span><span class="sxs-lookup"><span data-stu-id="934bf-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="934bf-166">Получение входного большого двоичного объекта, представляющего сетевую карту</span><span class="sxs-lookup"><span data-stu-id="934bf-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="934bf-167">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="934bf-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="934bf-168">Требования</span><span class="sxs-lookup"><span data-stu-id="934bf-168">Requirements</span></span>



| <span data-ttu-id="934bf-169">Требование</span><span class="sxs-lookup"><span data-stu-id="934bf-169">Requirement</span></span> | <span data-ttu-id="934bf-170">Значение</span><span class="sxs-lookup"><span data-stu-id="934bf-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="934bf-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="934bf-171">Minimum supported client</span></span><br/> | <span data-ttu-id="934bf-172">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="934bf-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="934bf-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="934bf-173">Minimum supported server</span></span><br/> | <span data-ttu-id="934bf-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="934bf-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="934bf-175">Заголовок</span><span class="sxs-lookup"><span data-stu-id="934bf-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="934bf-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="934bf-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="934bf-177">DLL</span><span class="sxs-lookup"><span data-stu-id="934bf-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="934bf-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="934bf-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="934bf-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="934bf-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934bf-180">истатс</span><span class="sxs-lookup"><span data-stu-id="934bf-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="934bf-181">Истатс:: Configure</span><span class="sxs-lookup"><span data-stu-id="934bf-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="934bf-182">Истатс::D подключение</span><span class="sxs-lookup"><span data-stu-id="934bf-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="934bf-183">сетевой монитор большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="934bf-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 





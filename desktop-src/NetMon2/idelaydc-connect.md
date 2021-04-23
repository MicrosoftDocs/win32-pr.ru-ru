---
description: Метод Connect подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации подключения.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'Метод Иделайдк:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896766"
---
# <a name="idelaydcconnect-method"></a><span data-ttu-id="0c5d7-103">Метод Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="0c5d7-103">IDelaydC::Connect method</span></span>

<span data-ttu-id="0c5d7-104">Метод **Connect** подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации подключения.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-104">The **Connect** method connects the NPP to the network by using a specified network interface card and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c5d7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="0c5d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c5d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c5d7-107">*хинпутблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c5d7-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5d7-108">Обработчик для большого двоичного объекта, указывающий сетевую карту, к которой вы подключаетесь, и сведения о конфигурации этого подключения.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information about that connection.</span></span>

</dd> <dt>

<span data-ttu-id="0c5d7-109">*Статускаллбаккпрок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c5d7-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5d7-110">Адрес функции обратного вызова пользователя, которая используется для получения обновлений состояния, таких как триггеры.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-110">Address of the user's callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="0c5d7-111">Если функция обратного вызова не используется, присвойте этому параметру и параметру *UserContext* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-111">If no callback function is used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0c5d7-112">*UserContext* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c5d7-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5d7-113">Значение, передаваемое при вызове функции обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="0c5d7-114">Значением этого параметра обычно является HWND или указатель this.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="0c5d7-115">Если функция обратного вызова не указана, присвойте этому параметру и параметру *Статускаллбаккпрок* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0c5d7-116">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0c5d7-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5d7-117">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c5d7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c5d7-118">Return value</span></span>

<span data-ttu-id="0c5d7-119">Если этот метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-119">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0c5d7-120">Если метод завершился неудачно, возвращаемое значение является одним из следующих кодов ошибок (которые содержат ошибки, возвращенные внутренним вызовом **иделайдк:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="0c5d7-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IDelaydC::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c5d7-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0c5d7-121">Return code</span></span></th>
<th><span data-ttu-id="0c5d7-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0c5d7-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="0c5d7-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-124">Этот экземпляр COM-объекта НПП уже подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0c5d7-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-126">Большой двоичный объект конфигурации поврежден.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="0c5d7-127">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-127">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0c5d7-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-129">Входной большой двоичный объект, заданный параметром <em>хинпутблоб</em> , не содержит записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-129">The input BLOB specified by <em>hInputBlob</em> is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="0c5d7-130">Эта ошибка может быть вызвана вызовом <strong>иделайдк:: Connect</strong> или <strong>Иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-130">This error may be generated by the <strong>IDelaydC::Connect</strong> or <strong>IDelaydC::Configure</strong> call.</span></span> <span data-ttu-id="0c5d7-131">Посмотрите на большой двоичный объект Error, возвращенный <em>херрорблоб</em> , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0c5d7-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-133">Функция <strong>CreateBlob</strong> не была вызвана.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="0c5d7-134">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-134">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0c5d7-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-136">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-136">The string is not null-terminated.</span></span> <span data-ttu-id="0c5d7-137">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-137">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0c5d7-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-139">Часть триггера входного большого двоичного объекта повреждена.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="0c5d7-140">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-140">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0c5d7-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-142">Объект, указанный в <em>хинпутблоб</em> , не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="0c5d7-143">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-143">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0c5d7-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-145">Каталог записи по умолчанию не был задан в реестре.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="0c5d7-146">Используйте следующий путь, чтобы задать каталог записи.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0c5d7-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-148">Недостаточно памяти для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-148">No memory was available to perform this operation.</span></span> <span data-ttu-id="0c5d7-149">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-149">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0c5d7-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-151">Время ожидания запроса истекло. Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-151">The request has timed out. This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0c5d7-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="0c5d7-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="0c5d7-153">Неверный номер версии большого двоичного объекта, указанного в <em>хинпутблоб</em> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="0c5d7-154">Эта ошибка возникает при вызове <strong>иделайдк:: Configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-154">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0c5d7-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c5d7-155">Remarks</span></span>

<span data-ttu-id="0c5d7-156">При вызове метода **Connect** НПП автоматически вызывает **Иделайдк:: Configure** с помощью большого двоичного объекта, предоставленного *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-156">When the **Connect** method is called, the NPP automatically calls **IDelaydC::Configure** by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="0c5d7-157">Обратите внимание, что все коды ошибок, возвращенные вызовом **иделайдк:: Configure** , передаются обратно и возвращаются вызовом **Иделайдк:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="0c5d7-157">Note that any error codes returned by the call to **IDelaydC::Configure** are passed back and returned by the **IDelaydC::Connect** call.</span></span>

<span data-ttu-id="0c5d7-158">Этот метод должен быть вызван до начала записи кадров.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="0c5d7-159">Обратите внимание, что при подключении к сети с помощью этого метода необходимо продолжить использование методов интерфейса **иделайдк** для записи кадров.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-159">Note that when you connect to the network by using this method, you must continue to use the **IDelaydC** interface methods to capture frames.</span></span>

<span data-ttu-id="0c5d7-160">Входной большой двоичный объект, заданный параметром *хинпутблоб* , можно получить, вызвав **жетнппблобфромуи**, **жетнппблобтабле** и **селектнппблобфромтабле**.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-160">The input BLOB specified by the *hInputBlob* parameter can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="0c5d7-161">BLOB-объект ошибки, возвращенный в *херрорблоб* , содержит сведения об ошибке, которые разработчик или приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-161">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="0c5d7-162">BLOB-объект ошибки, возвращенный *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти во входном большом двоичном объекте, указанном в *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-162">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="0c5d7-163">Например, если \_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует, запись, сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="0c5d7-164">Сведения о</span><span class="sxs-lookup"><span data-stu-id="0c5d7-164">For information about</span></span>                          | <span data-ttu-id="0c5d7-165">См.</span><span class="sxs-lookup"><span data-stu-id="0c5d7-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0c5d7-166">Получение входного большого двоичного объекта, представляющего сетевую карту</span><span class="sxs-lookup"><span data-stu-id="0c5d7-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="0c5d7-167">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="0c5d7-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="0c5d7-168">Требования</span><span class="sxs-lookup"><span data-stu-id="0c5d7-168">Requirements</span></span>



| <span data-ttu-id="0c5d7-169">Требование</span><span class="sxs-lookup"><span data-stu-id="0c5d7-169">Requirement</span></span> | <span data-ttu-id="0c5d7-170">Значение</span><span class="sxs-lookup"><span data-stu-id="0c5d7-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5d7-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c5d7-171">Minimum supported client</span></span><br/> | <span data-ttu-id="0c5d7-172">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0c5d7-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0c5d7-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c5d7-173">Minimum supported server</span></span><br/> | <span data-ttu-id="0c5d7-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0c5d7-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0c5d7-175">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0c5d7-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c5d7-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c5d7-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0c5d7-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0c5d7-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c5d7-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c5d7-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c5d7-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c5d7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5d7-180">иделайдк</span><span class="sxs-lookup"><span data-stu-id="0c5d7-180">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0c5d7-181">Иделайдк:: Configure</span><span class="sxs-lookup"><span data-stu-id="0c5d7-181">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="0c5d7-182">Иделайдк::D подключение</span><span class="sxs-lookup"><span data-stu-id="0c5d7-182">IDelaydC::Disconnect</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="0c5d7-183">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="0c5d7-183">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> </dl>

 

 





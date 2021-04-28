---
description: 'Метод ИРТК:: Connect. метод Connect подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации для подключения.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Метод ИРТК:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110748"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="c7049-103">Метод ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="c7049-103">IRTC::Connect method</span></span>

<span data-ttu-id="c7049-104">Метод **Connect** подключает НПП к сети с помощью указанной сетевой карты и предоставляет сведения о конфигурации для подключения.</span><span class="sxs-lookup"><span data-stu-id="c7049-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7049-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7049-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="c7049-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7049-107">*хинпутблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7049-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7049-108">Обработчик для большого двоичного объекта, указывающий сетевую карту, к которой вы подключаетесь, и сведения о конфигурации для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="c7049-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="c7049-109">*Статускаллбаккпрок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7049-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7049-110">Адрес функции обратного вызова состояния пользователя, которая получает обновления состояния, такие как триггеры.</span><span class="sxs-lookup"><span data-stu-id="c7049-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="c7049-111">Этому параметру можно присвоить **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7049-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c7049-112">*Фрамескаллбаккпрок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7049-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7049-113">Адрес функции обратного вызова кадра пользователя, которая используется для получения обновлений состояния, таких как триггеры.</span><span class="sxs-lookup"><span data-stu-id="c7049-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="c7049-114">Этому параметру можно присвоить **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7049-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c7049-115">*UserContext* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7049-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7049-116">Значение, передаваемое при вызове функции обратного вызова состояния пользователя и кадра.</span><span class="sxs-lookup"><span data-stu-id="c7049-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="c7049-117">Если указаны обе функции обратного вызова, они должны использовать одно и то же значение контекста пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7049-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="c7049-118">Значением этого параметра обычно является HWND или указатель this.</span><span class="sxs-lookup"><span data-stu-id="c7049-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="c7049-119">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7049-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7049-120">Обработайте с BLOB-объектом ошибок, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c7049-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="c7049-121">Сведения о том, что содержится в большом двоичном объекте с ошибками, см. в разделе Примечания в нижней части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="c7049-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7049-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7049-122">Return value</span></span>

<span data-ttu-id="c7049-123">Если этот метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c7049-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c7049-124">Если метод завершился неудачно, возвращаемое значение является одним из следующих кодов ошибок (которые содержат ошибки, возвращенные внутренним вызовом **ИРТК:: Configure** ):</span><span class="sxs-lookup"><span data-stu-id="c7049-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="c7049-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c7049-125">Return code</span></span>                                                                                                         | <span data-ttu-id="c7049-126">Описание</span><span class="sxs-lookup"><span data-stu-id="c7049-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7049-127"><dt>**НМЕРР \_ уже \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="c7049-128">Этот экземпляр COM-объекта НПП уже подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="c7049-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="c7049-129"><dt>**\_Ошибка преобразования BLOB-объекта нмерр \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="c7049-130">Большой двоичный объект конфигурации поврежден.</span><span class="sxs-lookup"><span data-stu-id="c7049-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="c7049-131">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c7049-132"><dt>**\_запись BLOB-объекта нмерр \_ \_ \_ не \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="c7049-133">Входной большой двоичный объект, заданный параметром *хинпутблоб* , не имеет записи, необходимой для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="c7049-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="c7049-134">Эта ошибка может быть вызвана вызовом **ИРТК:: Connect** или **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="c7049-135">Посмотрите на большой двоичный объект Error, возвращенный *херрорблоб* , чтобы определить, какая запись не найдена.</span><span class="sxs-lookup"><span data-stu-id="c7049-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="c7049-136"><dt>**\_BLOB-объект нмерр \_ не \_ инициализирован**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="c7049-137">Функция **CreateBlob** не была вызвана.</span><span class="sxs-lookup"><span data-stu-id="c7049-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="c7049-138">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="c7049-139"><dt>**\_ \_ Недопустимая строка большого двоичного объекта нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="c7049-140">Строка не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="c7049-140">The string is not null-terminated.</span></span> <span data-ttu-id="c7049-141">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c7049-142"><dt>**НМЕРР \_ Недопустимый \_ триггер**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="c7049-143">Часть триггера входного большого двоичного объекта повреждена.</span><span class="sxs-lookup"><span data-stu-id="c7049-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="c7049-144">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="c7049-145"><dt>**НМЕРР \_ Недопустимый \_ BLOB-объект**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="c7049-146">Объект, указанный в *хинпутблоб* , не является BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="c7049-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="c7049-147">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="c7049-148"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="c7049-149">Память, необходимая для выполнения этой операции, недоступна.</span><span class="sxs-lookup"><span data-stu-id="c7049-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="c7049-150">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="c7049-151"><dt>**\_время ожидания нмерр**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="c7049-152">Время ожидания запроса истекло. Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="c7049-153"><dt>**\_BLOB-объект верхнего уровня нмерр \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="c7049-154">Неверный номер версии большого двоичного объекта, указанного в *хинпутблоб* .</span><span class="sxs-lookup"><span data-stu-id="c7049-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="c7049-155">Эта ошибка возникает при вызове **ИРТК:: Configure** .</span><span class="sxs-lookup"><span data-stu-id="c7049-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="c7049-156">Remarks</span><span class="sxs-lookup"><span data-stu-id="c7049-156">Remarks</span></span>

<span data-ttu-id="c7049-157">При вызове метода **Connect** НПП автоматически вызывает метод **ИРТК:: Configure** с помощью большого двоичного объекта, предоставленного *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="c7049-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="c7049-158">Обратите внимание, что все коды ошибок, возвращенные вызовом **ИРТК:: Configure** , передаются обратно и возвращаются вызовом **ИРТК:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="c7049-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="c7049-159">Этот метод должен быть вызван до начала записи кадров.</span><span class="sxs-lookup"><span data-stu-id="c7049-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="c7049-160">Обратите внимание, что при подключении к сети с помощью этого метода необходимо продолжить использовать интерфейс **ИРТК** для записи кадров.</span><span class="sxs-lookup"><span data-stu-id="c7049-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="c7049-161">При вызове этой функции необходимо указать состояние или функцию обратного вызова кадра, даже если она действует только как заполнитель.</span><span class="sxs-lookup"><span data-stu-id="c7049-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="c7049-162">Входной большой двоичный объект, заданный параметром *хинпутблоб* , можно получить, вызвав методы **жетнппблобфромуи**, **жетнппблобтабле** и **селектнппблобфромтабле** .</span><span class="sxs-lookup"><span data-stu-id="c7049-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="c7049-163">BLOB-объект ошибки, возвращенный в *херрорблоб* , содержит сведения об ошибке, которые разработчик или приложение может использовать для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="c7049-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="c7049-164">BLOB-объект ошибки, возвращенный *херрорблоб* , содержит записи, которые сетевой монитор не удалось распознать или найти во входном большом двоичном объекте, указанном в *хинпутблоб*.</span><span class="sxs-lookup"><span data-stu-id="c7049-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="c7049-165">Например, если \_ запись BLOB-объекта нмерр \_ \_ \_ не \_ существует, запись, сетевой монитор не удалось найти, включается в возвращенный большой двоичный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="c7049-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="c7049-166">Сведения о</span><span class="sxs-lookup"><span data-stu-id="c7049-166">For information about</span></span>                          | <span data-ttu-id="c7049-167">См.</span><span class="sxs-lookup"><span data-stu-id="c7049-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c7049-168">Получение входного большого двоичного объекта, представляющего сетевую карту</span><span class="sxs-lookup"><span data-stu-id="c7049-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="c7049-169">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="c7049-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="c7049-170">Требования</span><span class="sxs-lookup"><span data-stu-id="c7049-170">Requirements</span></span>



| <span data-ttu-id="c7049-171">Требование</span><span class="sxs-lookup"><span data-stu-id="c7049-171">Requirement</span></span> | <span data-ttu-id="c7049-172">Значение</span><span class="sxs-lookup"><span data-stu-id="c7049-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7049-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7049-173">Minimum supported client</span></span><br/> | <span data-ttu-id="c7049-174">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7049-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c7049-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7049-175">Minimum supported server</span></span><br/> | <span data-ttu-id="c7049-176">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7049-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c7049-177">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c7049-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7049-178"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c7049-179">DLL</span><span class="sxs-lookup"><span data-stu-id="c7049-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7049-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7049-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7049-181">См. также</span><span class="sxs-lookup"><span data-stu-id="c7049-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7049-182">иртк</span><span class="sxs-lookup"><span data-stu-id="c7049-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c7049-183">ИРТК:: Configure</span><span class="sxs-lookup"><span data-stu-id="c7049-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="c7049-184">ИРТК::D подключение</span><span class="sxs-lookup"><span data-stu-id="c7049-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="c7049-185">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="c7049-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 





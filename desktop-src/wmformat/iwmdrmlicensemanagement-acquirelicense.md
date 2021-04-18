---
title: Метод Ивмдрмлиценсеманажемент AcquireLicense (Вмдрмсдк. h)
description: Метод AcquireLicense асинхронно получает лицензию с указанного URL-адреса.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Формат Windows Media, AcquireLicense метод
- AcquireLicense метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704385"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="91bde-106">Метод Ивмдрмлиценсеманажемент:: AcquireLicense</span><span class="sxs-lookup"><span data-stu-id="91bde-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="91bde-107">Метод **AcquireLicense** асинхронно получает лицензию с указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="91bde-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="91bde-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91bde-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="91bde-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="91bde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91bde-110">*бструрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91bde-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bde-111">URL-адрес сервера лицензирования, с которого будет получена лицензия.</span><span class="sxs-lookup"><span data-stu-id="91bde-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="91bde-112">Передайте **значение NULL** , чтобы метод анализировал URL-адрес из заголовка содержимого.</span><span class="sxs-lookup"><span data-stu-id="91bde-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="91bde-113">*бстрхеадердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91bde-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bde-114">Заголовок содержимого, передаваемый серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="91bde-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="91bde-115">Если *бструрл* имеет **значение NULL**, метод будет анализировать URL-адрес из этого заголовка.</span><span class="sxs-lookup"><span data-stu-id="91bde-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="91bde-116">Если для *dwFlags* задано значение \_ \_ устаревшей лицензии на получение сертификата WMDRM \_ \_ , задайте для этого параметра идентификатор ключа, а не весь заголовок содержимого.</span><span class="sxs-lookup"><span data-stu-id="91bde-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="91bde-117">*бстрактионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91bde-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bde-118">Строка, содержащая ноль или более действий, для которых запрашивается разрешение в лицензии.</span><span class="sxs-lookup"><span data-stu-id="91bde-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="91bde-119">Строка должна быть отформатирована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91bde-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="91bde-120">Каждое действие должно быть определено в элементе ACTION.</span><span class="sxs-lookup"><span data-stu-id="91bde-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="91bde-121">Данные элемента являются строкой действия.</span><span class="sxs-lookup"><span data-stu-id="91bde-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="91bde-122">Все элементы ACTION должны содержаться в элементе АКТИОНЛИСТ.</span><span class="sxs-lookup"><span data-stu-id="91bde-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="91bde-123">Например, строка для запроса лицензии на воспроизведение содержимого форматируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91bde-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="91bde-124">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91bde-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bde-125">Флаги параметров приобретения лицензии.</span><span class="sxs-lookup"><span data-stu-id="91bde-125">License acquisition option flags.</span></span> <span data-ttu-id="91bde-126">Задайте одну из констант в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="91bde-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="91bde-127">Константа</span><span class="sxs-lookup"><span data-stu-id="91bde-127">Constant</span></span>                                   | <span data-ttu-id="91bde-128">Описание</span><span class="sxs-lookup"><span data-stu-id="91bde-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91bde-129">\_Автоматическое получение \_ лицензии \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="91bde-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="91bde-130">Лицензия будет выдана непосредственно через Интернет без подтверждения от клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="91bde-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="91bde-131">\_неавтоматическая лицензия на получение WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="91bde-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="91bde-132">Подсистема DRM создаст запрос на лицензию, который будет возвращен асинхронно для отправки на сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="91bde-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="91bde-133">\_ \_ \_ устаревшая лицензия на получение WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="91bde-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="91bde-134">То же, что и для \_ \_ неавтоматической лицензии на получение WMDRM \_ , за исключением того, что будет создан запрос лицензии DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="91bde-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="91bde-135">*ппункканцелатионкукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91bde-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91bde-136">Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="91bde-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="91bde-137">Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="91bde-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91bde-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91bde-138">Return value</span></span>

<span data-ttu-id="91bde-139">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="91bde-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="91bde-140">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="91bde-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="91bde-141">Код возврата</span><span class="sxs-lookup"><span data-stu-id="91bde-141">Return code</span></span>                                                                          | <span data-ttu-id="91bde-142">Описание</span><span class="sxs-lookup"><span data-stu-id="91bde-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="91bde-143"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="91bde-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="91bde-144">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="91bde-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91bde-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91bde-145">Remarks</span></span>

<span data-ttu-id="91bde-146">Этот метод выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="91bde-146">This method executes asynchronously.</span></span> <span data-ttu-id="91bde-147">Он возвращает сразу после вызова, а затем создает событие **мевмдрмлиценсеаккуиситионкомплетед** после завершения обработки.</span><span class="sxs-lookup"><span data-stu-id="91bde-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="91bde-148">Для операций приобретения лицензий без вмешательства пользователя значение события, полученное путем вызова **имфмедиаевент:: GetValue** , является указателем **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="91bde-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="91bde-149">Чтобы получить экземпляр интерфейса [**ивмдрмнонсилентлиценсеакуиситион**](iwmdrmnonsilentlicenseaquisition.md) , можно вызвать метод **QueryInterface** полученного интерфейса **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="91bde-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="91bde-150">Дополнительные сведения об использовании асинхронных методов расширенных API-интерфейсов клиента DRM Windows Media см. [в разделе Использование модели событий Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="91bde-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91bde-151">Требования</span><span class="sxs-lookup"><span data-stu-id="91bde-151">Requirements</span></span>



| <span data-ttu-id="91bde-152">Требование</span><span class="sxs-lookup"><span data-stu-id="91bde-152">Requirement</span></span> | <span data-ttu-id="91bde-153">Значение</span><span class="sxs-lookup"><span data-stu-id="91bde-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91bde-154">Header</span><span class="sxs-lookup"><span data-stu-id="91bde-154">Header</span></span><br/>  | <dl> <span data-ttu-id="91bde-155"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="91bde-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="91bde-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91bde-156">Library</span></span><br/> | <dl> <span data-ttu-id="91bde-157"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91bde-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91bde-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91bde-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bde-159">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="91bde-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="91bde-160">**Автоматическое получение лицензий**</span><span class="sxs-lookup"><span data-stu-id="91bde-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 






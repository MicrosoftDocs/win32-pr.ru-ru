---
title: Метод Ивмдрмдевицеапп Женератеметерчалленже (Вмдрмдевицеапп. h)
description: Метод Женератеметерчалленже получает данные отслеживания использования с устройства.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Метод Женератеметерчалленже Windows Media диспетчер устройств
- Метод Женератеметерчалленже Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Женератеметерчалленже
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695017"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="f0e6f-106">Метод Ивмдрмдевицеапп:: Женератеметерчалленже</span><span class="sxs-lookup"><span data-stu-id="f0e6f-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="f0e6f-107">Метод **женератеметерчалленже** получает данные отслеживания использования с устройства.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e6f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0e6f-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="f0e6f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e6f-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0e6f-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e6f-111">Указатель на интерфейс [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="f0e6f-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="f0e6f-112">Если приложение передает **значение NULL**, то сведения об отслеживании, хранящиеся на компьютере, используются вместо сведений об отслеживании на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="f0e6f-113">*бстрметерцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0e6f-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e6f-114">Сертификат отслеживания приложения в виде **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="f0e6f-115">Это подписанный сертификат, полученный от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="f0e6f-116">*пбстрметерурл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0e6f-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e6f-117">URL-адрес, по которому должны отправляться данные измерения.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="f0e6f-118">Она выделяется Windows Media диспетчер устройств и должна быть свободна вызывающей стороной с помощью **сисфристринг**.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="f0e6f-119">*пбстрметердата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0e6f-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e6f-120">Данные контроля использования для отправки в службу измерения.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="f0e6f-121">Она выделяется Windows Media диспетчер устройств и должна быть свободна вызывающей стороной с помощью **сисфристринг**.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e6f-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0e6f-122">Return value</span></span>

<span data-ttu-id="f0e6f-123">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f0e6f-124">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f0e6f-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f0e6f-125">Return code</span></span>                                                                                                      | <span data-ttu-id="f0e6f-126">Описание</span><span class="sxs-lookup"><span data-stu-id="f0e6f-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0e6f-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="f0e6f-128">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="f0e6f-129"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="f0e6f-130">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="f0e6f-131"><dt>**DRM \_ E \_ инвалидксмлтаг**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="f0e6f-132">XML имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="f0e6f-133"><dt>**DRM \_ E \_ ноксмлклосетаг**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="f0e6f-134">XML имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="f0e6f-135"><dt>**DRM \_ E \_ ноксмлопентаг**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="f0e6f-136">XML имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="f0e6f-137"><dt>**DRM \_ E \_ ксмлнотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="f0e6f-138">Не удалось найти требуемый XML-тег.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f0e6f-139"><dt>**Ошибки с устройства**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="f0e6f-140">Любое количество ошибок на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f0e6f-141"><dt>**Ошибки клиента DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="f0e6f-142">Любое количество внутренних ошибок клиента DRM.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="f0e6f-143"><dt>**\_устройство NS E \_ не является \_ \_ \_ устройством WMDRM**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="f0e6f-144">Указанное устройство не является устройством, совместимым с DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0e6f-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0e6f-145">Remarks</span></span>

<span data-ttu-id="f0e6f-146">Перед вызовом этого метода приложение должно вызвать [**ивмдрмдевицеапп:: куеридевицестатус**](iwmdrmdeviceapp-querydevicestatus.md) или [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) , чтобы убедиться, что все компоненты DRM устройства обновлены.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="f0e6f-147">Этот метод может быть вызван только на устройстве, которое поддерживает Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="f0e6f-148">Полученный *пбстрметердата* данных должен быть отправлен на URL-адрес, заданный параметром *пбстрметерурл*.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="f0e6f-149">Убедитесь, что извлеченные данные кодируются в URL-адресе, поэтому они не изменяются во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="f0e6f-150">Дополнительные сведения см. [в разделе Обработка защищенного содержимого в приложении](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e6f-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="f0e6f-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="f0e6f-151">Examples</span></span>

<span data-ttu-id="f0e6f-152">В следующем примере кода C++ создается объект **вмдрмдевицеапп** , проверяется, является ли устройство устройством Windows Media DRM 10, что его часы точны, а затем запрашиваются данные о измерениях.</span><span class="sxs-lookup"><span data-stu-id="f0e6f-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="f0e6f-153">Требования</span><span class="sxs-lookup"><span data-stu-id="f0e6f-153">Requirements</span></span>



| <span data-ttu-id="f0e6f-154">Требование</span><span class="sxs-lookup"><span data-stu-id="f0e6f-154">Requirement</span></span> | <span data-ttu-id="f0e6f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f0e6f-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e6f-156">Header</span><span class="sxs-lookup"><span data-stu-id="f0e6f-156">Header</span></span><br/>  | <dl> <span data-ttu-id="f0e6f-157"><dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="f0e6f-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f0e6f-158">Library</span></span><br/> | <dl> <span data-ttu-id="f0e6f-159"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0e6f-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="f0e6f-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0e6f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e6f-161">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="f0e6f-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="f0e6f-162">**Интерфейс Ивмдмдевице**</span><span class="sxs-lookup"><span data-stu-id="f0e6f-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="f0e6f-163">**Интерфейс Ивмдрмдевицеапп**</span><span class="sxs-lookup"><span data-stu-id="f0e6f-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






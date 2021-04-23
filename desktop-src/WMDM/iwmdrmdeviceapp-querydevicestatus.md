---
title: Метод Ивмдрмдевицеапп Куеридевицестатус (Вмдрмдевицеапп. h)
description: Метод Куеридевицестатус запрашивает у устройства текущее состояние DRM и возможности.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Метод Куеридевицестатус Windows Media диспетчер устройств
- Метод Куеридевицестатус Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Куеридевицестатус
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695015"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="63b58-106">Метод Ивмдрмдевицеапп:: Куеридевицестатус</span><span class="sxs-lookup"><span data-stu-id="63b58-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="63b58-107">Метод **куеридевицестатус** запрашивает у устройства текущее состояние DRM и возможности.</span><span class="sxs-lookup"><span data-stu-id="63b58-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b58-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63b58-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="63b58-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="63b58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b58-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63b58-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63b58-111">Указатель на объект [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="63b58-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="63b58-112">*пдвстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63b58-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63b58-113">Ноль или более следующих значений **DWORD** , ОПИСЫВАЮЩИХ аспекты DRM устройства, в сочетании с побитовым **или**.</span><span class="sxs-lookup"><span data-stu-id="63b58-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="63b58-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="63b58-114">See Remarks.</span></span>



| <span data-ttu-id="63b58-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="63b58-115">Status</span></span>                      | <span data-ttu-id="63b58-116">Описание</span><span class="sxs-lookup"><span data-stu-id="63b58-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="63b58-117">\_исвмдрм устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="63b58-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="63b58-118">Устройство поддерживает Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="63b58-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="63b58-119">\_нидклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="63b58-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="63b58-120">Устройство не имеет безопасных часов.</span><span class="sxs-lookup"><span data-stu-id="63b58-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="63b58-121">\_устройство WMDRM \_ отозвано</span><span class="sxs-lookup"><span data-stu-id="63b58-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="63b58-122">Устройство было отозвано.</span><span class="sxs-lookup"><span data-stu-id="63b58-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="63b58-123">\_нидиндив клиента \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="63b58-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="63b58-124">Необходимо выполнить индивидуальную защиту DRM.</span><span class="sxs-lookup"><span data-stu-id="63b58-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="63b58-125">\_рефрешклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="63b58-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="63b58-126">Необходимо обновить часы.</span><span class="sxs-lookup"><span data-stu-id="63b58-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b58-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63b58-127">Return value</span></span>

<span data-ttu-id="63b58-128">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="63b58-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="63b58-129">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="63b58-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="63b58-130">Код возврата</span><span class="sxs-lookup"><span data-stu-id="63b58-130">Return code</span></span>                                                                                                              | <span data-ttu-id="63b58-131">Описание</span><span class="sxs-lookup"><span data-stu-id="63b58-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63b58-132"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="63b58-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="63b58-133">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="63b58-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="63b58-134"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63b58-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="63b58-135">Недопустимый входной аргумент.</span><span class="sxs-lookup"><span data-stu-id="63b58-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="63b58-136"><dt>**\_ \_ \_ Недопустимый \_ сертификат DRM в NS E**</dt></span><span class="sxs-lookup"><span data-stu-id="63b58-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="63b58-137">Сертификат устройства, полученный с устройства, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="63b58-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="63b58-138"><dt>**системе \_ \_ управления правами NS \_ не удалось \_ \_ получить \_ \_ сертификат устройства**</dt></span><span class="sxs-lookup"><span data-stu-id="63b58-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="63b58-139">Не удалось получить сертификат устройства с устройства.</span><span class="sxs-lookup"><span data-stu-id="63b58-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="63b58-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63b58-140">Remarks</span></span>

<span data-ttu-id="63b58-141">Этот метод следует вызывать перед выполнением каких либо ограниченных действий с содержимым DRM, например для передачи содержимого DRM на устройство или получения сведений о метриках.</span><span class="sxs-lookup"><span data-stu-id="63b58-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="63b58-142">Если значения, полученные с помощью *пдвстатус* , указывают на необходимость выполнения какого-либо действия (например, для настольного компьютера или получения часов для устройства), приложение должно вызвать [**аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md) и передать полученное значение *пдвстатус* из этой функции в параметр *dwFlags* в **аккуиредевицедата**.</span><span class="sxs-lookup"><span data-stu-id="63b58-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="63b58-143">Если возвращается нуль, устройство не поддерживает Windows Media DRM 10 для переносных устройств, и никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="63b58-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="63b58-144">Дополнительные сведения см. [в разделе Обработка защищенного содержимого в приложении](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="63b58-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="63b58-145">Примеры</span><span class="sxs-lookup"><span data-stu-id="63b58-145">Examples</span></span>

<span data-ttu-id="63b58-146">В следующем примере кода C++ создается объект **вмдрмдевицеапп** , проверяется, является ли устройство устройством Windows Media DRM 10, что его часы точны, а затем запрашиваются данные о измерениях.</span><span class="sxs-lookup"><span data-stu-id="63b58-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="63b58-147">Требования</span><span class="sxs-lookup"><span data-stu-id="63b58-147">Requirements</span></span>



| <span data-ttu-id="63b58-148">Требование</span><span class="sxs-lookup"><span data-stu-id="63b58-148">Requirement</span></span> | <span data-ttu-id="63b58-149">Значение</span><span class="sxs-lookup"><span data-stu-id="63b58-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b58-150">Header</span><span class="sxs-lookup"><span data-stu-id="63b58-150">Header</span></span><br/>  | <dl> <span data-ttu-id="63b58-151"><dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="63b58-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="63b58-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63b58-152">Library</span></span><br/> | <dl> <span data-ttu-id="63b58-153"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63b58-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="63b58-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63b58-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b58-155">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="63b58-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="63b58-156">**Интерфейс Ивмдрмдевицеапп**</span><span class="sxs-lookup"><span data-stu-id="63b58-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="63b58-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="63b58-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 






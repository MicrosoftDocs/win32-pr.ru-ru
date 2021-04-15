---
title: Метод IWMDRMDeviceApp2 QueryDeviceStatus2 (Вмдрмдевицеапп. h)
description: Метод QueryDeviceStatus2 запрашивает устройство для определенного состояния DRM или возможности.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Метод QueryDeviceStatus2 Windows Media диспетчер устройств
- Метод QueryDeviceStatus2 Windows Media диспетчер устройств, интерфейс IWMDRMDeviceApp2
- Интерфейс IWMDRMDeviceApp2 Windows Media диспетчер устройств, метод QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695138"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="728cf-106">Метод IWMDRMDeviceApp2:: QueryDeviceStatus2</span><span class="sxs-lookup"><span data-stu-id="728cf-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="728cf-107">Метод **QueryDeviceStatus2** запрашивает устройство для определенного состояния DRM или возможности.</span><span class="sxs-lookup"><span data-stu-id="728cf-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="728cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="728cf-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="728cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="728cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="728cf-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="728cf-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="728cf-111">Указатель на объект [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="728cf-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="728cf-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="728cf-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="728cf-113">Одно или несколько из следующих значений **DWORD** , указывающих, какие возможности необходимо запросить, в сочетании с побитовым **или**.</span><span class="sxs-lookup"><span data-stu-id="728cf-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="728cf-114">Flag</span><span class="sxs-lookup"><span data-stu-id="728cf-114">Flag</span></span>                              | <span data-ttu-id="728cf-115">Описание</span><span class="sxs-lookup"><span data-stu-id="728cf-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="728cf-116">\_ \_ ИНДИВСТАТУС клиента WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="728cf-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="728cf-117">Запросите, должны ли быть индивидуальными компоненты DRM компьютера.</span><span class="sxs-lookup"><span data-stu-id="728cf-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="728cf-118">\_ \_ клоккстатус устройства для запросов WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="728cf-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="728cf-119">Запрос на то, нужно ли добавлять или обновлять безопасное время устройства.</span><span class="sxs-lookup"><span data-stu-id="728cf-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="728cf-120">\_ \_ аннулирование устройства с ЗАПРОСом WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="728cf-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="728cf-121">Запрос на то, отозвано ли устройство.</span><span class="sxs-lookup"><span data-stu-id="728cf-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="728cf-122">\_ \_ исвмдрм устройства для запросов WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="728cf-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="728cf-123">Запросите, поддерживает ли устройство Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="728cf-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="728cf-124">*пдвстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="728cf-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="728cf-125">Ноль или более следующих значений **DWORD** , указывающих запрошенное состояние устройства, в сочетании с побитовым **или**.</span><span class="sxs-lookup"><span data-stu-id="728cf-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="728cf-126">Состояние</span><span class="sxs-lookup"><span data-stu-id="728cf-126">Status</span></span>                      | <span data-ttu-id="728cf-127">Описание</span><span class="sxs-lookup"><span data-stu-id="728cf-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="728cf-128">\_исвмдрм устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="728cf-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="728cf-129">Устройство поддерживает Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="728cf-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="728cf-130">\_нидклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="728cf-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="728cf-131">Устройство не имеет безопасных часов.</span><span class="sxs-lookup"><span data-stu-id="728cf-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="728cf-132">\_устройство WMDRM \_ отозвано</span><span class="sxs-lookup"><span data-stu-id="728cf-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="728cf-133">Устройство было отозвано.</span><span class="sxs-lookup"><span data-stu-id="728cf-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="728cf-134">\_нидиндив клиента \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="728cf-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="728cf-135">Компоненты DRM компьютера должны быть индивидуальными.</span><span class="sxs-lookup"><span data-stu-id="728cf-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="728cf-136">\_рефрешклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="728cf-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="728cf-137">Необходимо обновить часы.</span><span class="sxs-lookup"><span data-stu-id="728cf-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="728cf-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="728cf-138">Return value</span></span>

<span data-ttu-id="728cf-139">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="728cf-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="728cf-140">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="728cf-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="728cf-141">Код возврата</span><span class="sxs-lookup"><span data-stu-id="728cf-141">Return code</span></span>                                                                                                              | <span data-ttu-id="728cf-142">Описание</span><span class="sxs-lookup"><span data-stu-id="728cf-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="728cf-143"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="728cf-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="728cf-144">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="728cf-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="728cf-145"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="728cf-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="728cf-146">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="728cf-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="728cf-147"><dt>**\_ \_ \_ Недопустимый \_ сертификат DRM в NS E**</dt></span><span class="sxs-lookup"><span data-stu-id="728cf-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="728cf-148">Сертификат устройства, полученный с устройства, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="728cf-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="728cf-149"><dt>**системе \_ \_ управления правами NS \_ не удалось \_ \_ получить \_ \_ сертификат устройства**</dt></span><span class="sxs-lookup"><span data-stu-id="728cf-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="728cf-150">Не удалось получить сертификат устройства с устройства.</span><span class="sxs-lookup"><span data-stu-id="728cf-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="728cf-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="728cf-151">Remarks</span></span>

<span data-ttu-id="728cf-152">Этот метод следует вызывать перед выполнением каких либо ограниченных действий с содержимым DRM, например для передачи содержимого DRM на устройство или получения сведений о метриках.</span><span class="sxs-lookup"><span data-stu-id="728cf-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="728cf-153">Если значения, полученные с помощью *пдвстатус* , указывают на необходимость выполнения какого-либо действия (например, для настольного компьютера или получения часов для устройства), приложение должно вызвать [**Ивмдрмдевицеапп:: аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md) и передать полученное значение *пдвстатус* из этой функции в параметр *dwFlags* в **аккуиредевицедата**.</span><span class="sxs-lookup"><span data-stu-id="728cf-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="728cf-154">Если возвращается нуль, устройство не поддерживает Windows Media DRM 10 для переносных устройств, и никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="728cf-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="728cf-155">Дополнительные сведения см. [в разделе Обработка защищенного содержимого в приложении](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="728cf-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="728cf-156">Требования</span><span class="sxs-lookup"><span data-stu-id="728cf-156">Requirements</span></span>



| <span data-ttu-id="728cf-157">Требование</span><span class="sxs-lookup"><span data-stu-id="728cf-157">Requirement</span></span> | <span data-ttu-id="728cf-158">Значение</span><span class="sxs-lookup"><span data-stu-id="728cf-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="728cf-159">Header</span><span class="sxs-lookup"><span data-stu-id="728cf-159">Header</span></span><br/>  | <dl> <span data-ttu-id="728cf-160"><dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="728cf-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="728cf-161">Библиотека</span><span class="sxs-lookup"><span data-stu-id="728cf-161">Library</span></span><br/> | <dl> <span data-ttu-id="728cf-162"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="728cf-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="728cf-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="728cf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728cf-164">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="728cf-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="728cf-165">**Ивмдрмдевицеапп:: Куеридевицестатус**</span><span class="sxs-lookup"><span data-stu-id="728cf-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="728cf-166">**Интерфейс IWMDRMDeviceApp2**</span><span class="sxs-lookup"><span data-stu-id="728cf-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 






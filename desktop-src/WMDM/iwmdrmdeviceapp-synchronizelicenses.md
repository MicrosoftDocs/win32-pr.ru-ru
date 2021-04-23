---
title: Метод Ивмдрмдевицеапп Синчронизелиценсес (Вмдрмдевицеапп. h)
description: Метод Синчронизелиценсес обновляет лицензии на устройстве, когда срок их действия приближается к истечению.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Метод Синчронизелиценсес Windows Media диспетчер устройств
- Метод Синчронизелиценсес Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Синчронизелиценсес
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695139"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="62f1d-106">Метод Ивмдрмдевицеапп:: Синчронизелиценсес</span><span class="sxs-lookup"><span data-stu-id="62f1d-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="62f1d-107">Метод **синчронизелиценсес** обновляет лицензии на устройстве, когда срок их действия приближается к истечению.</span><span class="sxs-lookup"><span data-stu-id="62f1d-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f1d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62f1d-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="62f1d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="62f1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62f1d-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62f1d-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62f1d-111">Указатель на объект [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="62f1d-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="62f1d-112">*ппрогресскаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62f1d-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62f1d-113">Обратный вызов хода выполнения, который получит ход выполнения всех шагов, которые может потребоваться выполнить. Шаг определяется параметром *EventID* метода [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) с именем.</span><span class="sxs-lookup"><span data-stu-id="62f1d-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="62f1d-114">*кминкаунтсрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62f1d-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62f1d-115">Необязательный минимально оставшийся Счетчик воспроизведения для лицензии устройства.</span><span class="sxs-lookup"><span data-stu-id="62f1d-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="62f1d-116">*кминхаурссрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62f1d-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62f1d-117">Необязательно минимальное количество оставшихся часов для лицензии устройства.</span><span class="sxs-lookup"><span data-stu-id="62f1d-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62f1d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62f1d-118">Return value</span></span>

<span data-ttu-id="62f1d-119">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="62f1d-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="62f1d-120">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="62f1d-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="62f1d-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62f1d-121">Return code</span></span>                                                                                                         | <span data-ttu-id="62f1d-122">Описание</span><span class="sxs-lookup"><span data-stu-id="62f1d-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62f1d-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="62f1d-124">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="62f1d-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="62f1d-125"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="62f1d-126">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="62f1d-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="62f1d-127"><dt>**DRM \_ E \_ инвалидксмлтаг**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="62f1d-128">XML имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="62f1d-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="62f1d-129"><dt>**DRM \_ E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="62f1d-130">Эта функция в настоящее время не реализована.</span><span class="sxs-lookup"><span data-stu-id="62f1d-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="62f1d-131">(Синклиценсес w/ *пдевице* = null)</span><span class="sxs-lookup"><span data-stu-id="62f1d-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="62f1d-132"><dt>**DRM \_ E \_ ноксмлклосетаг**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="62f1d-133">XML-файл лицензии был сформирован неправильно.</span><span class="sxs-lookup"><span data-stu-id="62f1d-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="62f1d-134"><dt>**DRM \_ E \_ ноксмлопентаг**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="62f1d-135">XML-файл лицензии был сформирован неправильно.</span><span class="sxs-lookup"><span data-stu-id="62f1d-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="62f1d-136"><dt>**DRM \_ E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="62f1d-137">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="62f1d-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="62f1d-138"><dt>**DRM \_ E \_ ксмлнотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="62f1d-139">Не удалось найти необходимый XML-тег в лицензии.</span><span class="sxs-lookup"><span data-stu-id="62f1d-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="62f1d-140"><dt>**\_устройство NS E \_ не является \_ \_ \_ устройством WMDRM**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="62f1d-141">Указанное устройство не является устройством, совместимым с Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="62f1d-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="62f1d-142"><dt>**для \_ \_ управления цифровыми правами (NS) \_ требуется \_ индивидуальность**</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="62f1d-143">Для выполнения этой функции DRM требуется отдельный черный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="62f1d-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="62f1d-144">Иными словами, для пакета SDK Windows Media Format требуется обновление системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="62f1d-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62f1d-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62f1d-145">Remarks</span></span>

<span data-ttu-id="62f1d-146">Этот вызов может выполняться только на устройстве, которое поддерживает Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="62f1d-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="62f1d-147">Необходимо указать хотя бы один параметр порога.</span><span class="sxs-lookup"><span data-stu-id="62f1d-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f1d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="62f1d-148">Requirements</span></span>



| <span data-ttu-id="62f1d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="62f1d-149">Requirement</span></span> | <span data-ttu-id="62f1d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="62f1d-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f1d-151">Header</span><span class="sxs-lookup"><span data-stu-id="62f1d-151">Header</span></span><br/>  | <dl> <span data-ttu-id="62f1d-152"><dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="62f1d-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62f1d-153">Library</span></span><br/> | <dl> <span data-ttu-id="62f1d-154"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62f1d-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="62f1d-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62f1d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f1d-156">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="62f1d-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="62f1d-157">**Интерфейс IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="62f1d-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="62f1d-158">**Интерфейс Ивмдрмдевицеапп**</span><span class="sxs-lookup"><span data-stu-id="62f1d-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






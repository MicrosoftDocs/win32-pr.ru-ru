---
title: Метод Ивмдрмдевицеапп Аккуиредевицедата (Вмдрмдевицеапп. h)
description: Метод Аккуиредевицедата Инициализирует или сбрасывает защищенные часы устройства.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Метод Аккуиредевицедата Windows Media диспетчер устройств
- Метод Аккуиредевицедата Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Аккуиредевицедата
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695018"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="b7dea-106">Метод Ивмдрмдевицеапп:: Аккуиредевицедата</span><span class="sxs-lookup"><span data-stu-id="b7dea-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="b7dea-107">Метод **аккуиредевицедата** Инициализирует или сбрасывает защищенные часы устройства.</span><span class="sxs-lookup"><span data-stu-id="b7dea-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7dea-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7dea-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b7dea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7dea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7dea-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7dea-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dea-111">Указатель на интерфейс [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) для устройства, которое будет сообщать данные об измерениях.</span><span class="sxs-lookup"><span data-stu-id="b7dea-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="b7dea-112">*ппрогресскаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7dea-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dea-113">Обратный вызов хода выполнения, с помощью которого приложение может отслеживать ход выполнения события или отменять событие.</span><span class="sxs-lookup"><span data-stu-id="b7dea-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="b7dea-114">Ход выполнения определяется параметром *EventID* методов [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .</span><span class="sxs-lookup"><span data-stu-id="b7dea-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="b7dea-115">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7dea-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dea-116">Логическое **или** для одного или обоих из следующих флагов, указывающих действие, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b7dea-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="b7dea-117">Это значение извлекается из параметра *Пдвстатус* [**Ивмдрмдевицеапп:: куеридевицестатус**](iwmdrmdeviceapp-querydevicestatus.md) или [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="b7dea-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="b7dea-118">Флаг *пдвстатус* можно использовать напрямую.</span><span class="sxs-lookup"><span data-stu-id="b7dea-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="b7dea-119">Flag</span><span class="sxs-lookup"><span data-stu-id="b7dea-119">Flag</span></span>                        | <span data-ttu-id="b7dea-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b7dea-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="b7dea-121">\_нидклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="b7dea-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="b7dea-122">Получение часов с сервера безопасных часов.</span><span class="sxs-lookup"><span data-stu-id="b7dea-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="b7dea-123">\_рефрешклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="b7dea-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="b7dea-124">Обновите часы с сервера безопасных часов.</span><span class="sxs-lookup"><span data-stu-id="b7dea-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b7dea-125">*пдвстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b7dea-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dea-126">Одно из следующих значений **DWORD** , указывающее состояние, возвращаемое устройством.</span><span class="sxs-lookup"><span data-stu-id="b7dea-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="b7dea-127">Состояние</span><span class="sxs-lookup"><span data-stu-id="b7dea-127">Status</span></span> | <span data-ttu-id="b7dea-128">Описание</span><span class="sxs-lookup"><span data-stu-id="b7dea-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="b7dea-129">0</span><span class="sxs-lookup"><span data-stu-id="b7dea-129">0</span></span>      | <span data-ttu-id="b7dea-130">Действие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7dea-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="b7dea-131">1</span><span class="sxs-lookup"><span data-stu-id="b7dea-131">1</span></span>      | <span data-ttu-id="b7dea-132">Не удалось получить защищенные часы устройства от службы.</span><span class="sxs-lookup"><span data-stu-id="b7dea-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="b7dea-133">2</span><span class="sxs-lookup"><span data-stu-id="b7dea-133">2</span></span>      | <span data-ttu-id="b7dea-134">Не удалось установить защищенное время устройства.</span><span class="sxs-lookup"><span data-stu-id="b7dea-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="b7dea-135">3</span><span class="sxs-lookup"><span data-stu-id="b7dea-135">3</span></span>      | <span data-ttu-id="b7dea-136">Установлено безопасное время устройства.</span><span class="sxs-lookup"><span data-stu-id="b7dea-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7dea-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7dea-137">Return value</span></span>

<span data-ttu-id="b7dea-138">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b7dea-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b7dea-139">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b7dea-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b7dea-140">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b7dea-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="b7dea-141">Описание</span><span class="sxs-lookup"><span data-stu-id="b7dea-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7dea-142"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="b7dea-143">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b7dea-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="b7dea-144"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="b7dea-145">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b7dea-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="b7dea-146"><dt>**\_устройство NS E \_ не является \_ \_ \_ устройством WMDRM**</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="b7dea-147">Указанное устройство не является устройством, совместимым с DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7dea-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b7dea-148"><dt>**системе \_ \_ управления цифровыми правами (DRM) \_ не удалось \_ \_ получить \_ защищенные \_ Часы**</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="b7dea-149">Не удалось получить из устройства запрос на безопасное время или не удалось получить URL-адрес защищенного времени.</span><span class="sxs-lookup"><span data-stu-id="b7dea-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="b7dea-150"><dt>**системе \_ \_ управления цифровыми правами (DRM) \_ не удалось \_ \_ получить \_ защищенные \_ часы \_ с \_ сервера**</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="b7dea-151">Не удалось получить отклик на безопасное время с сервера безопасных часов.</span><span class="sxs-lookup"><span data-stu-id="b7dea-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b7dea-152"><dt>**системе \_ \_ управления цифровыми правами (DRM) \_ не удалось \_ \_ установить \_ безопасные \_ Часы**</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="b7dea-153">Не удалось отправить запрос на безопасное время на устройство, или устройству не удалось установить часы.</span><span class="sxs-lookup"><span data-stu-id="b7dea-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="b7dea-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7dea-154">Remarks</span></span>

<span data-ttu-id="b7dea-155">Это асинхронный метод. Прежде чем пытаться воспроизвести лицензированное содержимое, устройство должно ожидать обратного вызова [**ивмдмпрогресс:: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) для этой операции.</span><span class="sxs-lookup"><span data-stu-id="b7dea-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="b7dea-156">Приложение может узнать, нужно ли сбрасывать или обновить часы на устройстве, вызвав [**ивмдрмдевицеапп:: куеридевицестатус**](iwmdrmdeviceapp-querydevicestatus.md) или [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="b7dea-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="b7dea-157">Приложение должно иметь подключение к Интернету, чтобы позволить ему получать или сбрасывать безопасные часы.</span><span class="sxs-lookup"><span data-stu-id="b7dea-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7dea-158">Требования</span><span class="sxs-lookup"><span data-stu-id="b7dea-158">Requirements</span></span>



| <span data-ttu-id="b7dea-159">Требование</span><span class="sxs-lookup"><span data-stu-id="b7dea-159">Requirement</span></span> | <span data-ttu-id="b7dea-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dea-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dea-161">Header</span><span class="sxs-lookup"><span data-stu-id="b7dea-161">Header</span></span><br/>  | <dl> <span data-ttu-id="b7dea-162"><dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="b7dea-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7dea-163">Library</span></span><br/> | <dl> <span data-ttu-id="b7dea-164"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7dea-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="b7dea-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7dea-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7dea-166">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="b7dea-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="b7dea-167">**Интерфейс Ивмдмдевице**</span><span class="sxs-lookup"><span data-stu-id="b7dea-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="b7dea-168">**Интерфейс IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="b7dea-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="b7dea-169">**Интерфейс Ивмдрмдевицеапп**</span><span class="sxs-lookup"><span data-stu-id="b7dea-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






---
title: Метод Ивмдрмдевицеапп Процессметерреспонсе (Вмдрмдевицеапп. h)
description: Метод Процессметерреспонсе сбрасывает некоторые или все счетчики контроля использования на устройстве, после того как данные с устройства были отправлены и обработаны сервером.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Метод Процессметерреспонсе Windows Media диспетчер устройств
- Метод Процессметерреспонсе Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Процессметерреспонсе
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695016"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="cbf49-106">Ивмдрмдевицеапп: метод:P Роцессметерреспонсе</span><span class="sxs-lookup"><span data-stu-id="cbf49-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="cbf49-107">Метод **процессметерреспонсе** сбрасывает некоторые или все счетчики контроля использования на устройстве, после того как данные с устройства были отправлены и обработаны сервером.</span><span class="sxs-lookup"><span data-stu-id="cbf49-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf49-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbf49-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cbf49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbf49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf49-110">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbf49-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf49-111">Указатель на объект [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="cbf49-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbf49-112">*пбреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbf49-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf49-113">Ответ, полученный от сервера отслеживания, после отправки данных, созданных с помощью [**женератеметерчалленже**](iwmdrmdeviceapp-generatemeterchallenge.md).</span><span class="sxs-lookup"><span data-stu-id="cbf49-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbf49-114">*кбреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbf49-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf49-115">Размер *пбреспонсе* в байтах.</span><span class="sxs-lookup"><span data-stu-id="cbf49-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cbf49-116">*пдвфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbf49-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf49-117">Значение **типа DWORD** из следующей таблицы, указывающее, имеются ли дополнительные данные метрик на устройстве, которое необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="cbf49-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="cbf49-118">Flag</span><span class="sxs-lookup"><span data-stu-id="cbf49-118">Flag</span></span>                            | <span data-ttu-id="cbf49-119">Описание</span><span class="sxs-lookup"><span data-stu-id="cbf49-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="cbf49-120">\_ответ от метрики WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="cbf49-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="cbf49-121">Все данные отслеживания использования обработаны.</span><span class="sxs-lookup"><span data-stu-id="cbf49-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="cbf49-122">\_ \_ частичный отклик на отслеживание WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="cbf49-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="cbf49-123">Необходимо обработать дополнительные данные отслеживания использования.</span><span class="sxs-lookup"><span data-stu-id="cbf49-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf49-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbf49-124">Return value</span></span>

<span data-ttu-id="cbf49-125">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cbf49-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cbf49-126">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cbf49-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cbf49-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cbf49-127">Return code</span></span>                                                                                                      | <span data-ttu-id="cbf49-128">Описание</span><span class="sxs-lookup"><span data-stu-id="cbf49-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbf49-129"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="cbf49-130">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="cbf49-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="cbf49-131"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="cbf49-132">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="cbf49-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="cbf49-133"><dt>**Ошибки с устройства**</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="cbf49-134">Любое количество ошибок на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cbf49-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="cbf49-135"><dt>**Ошибки клиента DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="cbf49-136">Любое количество внутренних ошибок клиента DRM.</span><span class="sxs-lookup"><span data-stu-id="cbf49-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="cbf49-137"><dt>**\_устройство NS E \_ не является \_ \_ \_ устройством WMDRM**</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="cbf49-138">Указанное устройство не является устройством, совместимым с DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cbf49-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbf49-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbf49-139">Remarks</span></span>

<span data-ttu-id="cbf49-140">Дополнительные сведения о измерениях, включая примеры кода, можно найти в техническом документе об [использовании цифрового мультимедиа с Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) на веб-сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="cbf49-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf49-141">Требования</span><span class="sxs-lookup"><span data-stu-id="cbf49-141">Requirements</span></span>



| <span data-ttu-id="cbf49-142">Требование</span><span class="sxs-lookup"><span data-stu-id="cbf49-142">Requirement</span></span> | <span data-ttu-id="cbf49-143">Значение</span><span class="sxs-lookup"><span data-stu-id="cbf49-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf49-144">Header</span><span class="sxs-lookup"><span data-stu-id="cbf49-144">Header</span></span><br/>  | <dl> <span data-ttu-id="cbf49-145"><dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="cbf49-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbf49-146">Library</span></span><br/> | <dl> <span data-ttu-id="cbf49-147"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="cbf49-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbf49-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf49-149">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="cbf49-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="cbf49-150">**Интерфейс Ивмдмдевице**</span><span class="sxs-lookup"><span data-stu-id="cbf49-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="cbf49-151">**Интерфейс Ивмдрмдевицеапп**</span><span class="sxs-lookup"><span data-stu-id="cbf49-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 


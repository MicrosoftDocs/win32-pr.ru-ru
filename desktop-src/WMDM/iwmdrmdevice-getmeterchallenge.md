---
title: Ивмдрмдевице Жетметерчалленже, метод
description: Метод Жетметерчалленже извлекает запрос контроля использования.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Метод Жетметерчалленже Windows Media диспетчер устройств
- Метод Жетметерчалленже Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетметерчалленже
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694421"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="e7d50-106">Метод Ивмдрмдевице:: Жетметерчалленже</span><span class="sxs-lookup"><span data-stu-id="e7d50-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="e7d50-107">Метод **жетметерчалленже** извлекает запрос контроля использования.</span><span class="sxs-lookup"><span data-stu-id="e7d50-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d50-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7d50-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="e7d50-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7d50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d50-110">*бстрметерцерт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7d50-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d50-111">Сертификат контроля использования, который владелец содержимого отправляет на главный компьютер для сбора данных об измерении, связанных с измерением на устройстве</span><span class="sxs-lookup"><span data-stu-id="e7d50-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="e7d50-112">*ппбметерчалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e7d50-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d50-113">Получен результат запроса контроля использования.</span><span class="sxs-lookup"><span data-stu-id="e7d50-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="e7d50-114">*пкбметерчалленже* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e7d50-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d50-115">Размер задачи отслеживания в байтах.</span><span class="sxs-lookup"><span data-stu-id="e7d50-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d50-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7d50-116">Return value</span></span>

<span data-ttu-id="e7d50-117">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7d50-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7d50-118">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e7d50-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7d50-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e7d50-119">Return code</span></span>                                                                          | <span data-ttu-id="e7d50-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e7d50-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7d50-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e7d50-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7d50-122">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e7d50-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7d50-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7d50-123">Remarks</span></span>

<span data-ttu-id="e7d50-124">Данные контроля использования собираются и сохраняются в хранилище данных DRM на устройстве для содержимого с включенным измерением.</span><span class="sxs-lookup"><span data-stu-id="e7d50-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="e7d50-125">Будут записаны такие действия, как воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="e7d50-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="e7d50-126">При вызове этой функции устройство собирает данные об измерениях в хранилище данных DRM в виде XML-документа и отправляет их в хосткомпутер.</span><span class="sxs-lookup"><span data-stu-id="e7d50-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="e7d50-127">Если объем данных слишком большой, он отправляется поэтапно.</span><span class="sxs-lookup"><span data-stu-id="e7d50-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="e7d50-128">Когда главный компьютер получает данные отслеживания использования, он отправляет данные через Интернет по URL-адресу, указанному в сертификате измерения.</span><span class="sxs-lookup"><span data-stu-id="e7d50-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d50-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e7d50-129">Requirements</span></span>



| <span data-ttu-id="e7d50-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e7d50-130">Requirement</span></span> | <span data-ttu-id="e7d50-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e7d50-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d50-132">Header</span><span class="sxs-lookup"><span data-stu-id="e7d50-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e7d50-133"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7d50-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="e7d50-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7d50-134">Library</span></span><br/> | <dl> <span data-ttu-id="e7d50-135"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7d50-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d50-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7d50-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d50-137">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="e7d50-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 






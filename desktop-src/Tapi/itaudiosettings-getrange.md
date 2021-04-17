---
description: Метод дальнего действия извлекает диапазон допустимых значений для заданного свойства звуковых параметров.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: Метод Итаудиосеттингс::-Range (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685208"
---
# <a name="itaudiosettingsgetrange-method"></a><span data-ttu-id="2b282-103">Метод Итаудиосеттингс:: Range</span><span class="sxs-lookup"><span data-stu-id="2b282-103">ITAudioSettings::GetRange method</span></span>

<span data-ttu-id="2b282-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2b282-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2b282-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="2b282-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2b282-106">Метод **дальнего действия** извлекает диапазон допустимых значений для заданного [**Свойства звуковых параметров**](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="2b282-106">The **GetRange** method retrieves the range of valid values for a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b282-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b282-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="2b282-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b282-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b282-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b282-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b282-110">Член перечисления [**аудиосеттингспроперти**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2b282-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="2b282-111">*плмин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b282-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b282-112">Минимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="2b282-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="2b282-113">*плмакс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b282-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b282-114">Максимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="2b282-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="2b282-115">*плстеппингделта* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b282-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b282-116">Шаг приращения, на который может увеличиться или уменьшиться значение свойства.</span><span class="sxs-lookup"><span data-stu-id="2b282-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="2b282-117">*плдефаулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b282-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b282-118">Значение по умолчанию для параметра *Property* .</span><span class="sxs-lookup"><span data-stu-id="2b282-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2b282-119">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b282-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b282-120">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="2b282-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b282-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b282-121">Return value</span></span>

<span data-ttu-id="2b282-122">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2b282-122">This method can return one of these values.</span></span>



| <span data-ttu-id="2b282-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2b282-123">Return code</span></span>                                                                                   | <span data-ttu-id="2b282-124">Описание</span><span class="sxs-lookup"><span data-stu-id="2b282-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2b282-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2b282-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2b282-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2b282-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2b282-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2b282-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2b282-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2b282-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b282-129">Требования</span><span class="sxs-lookup"><span data-stu-id="2b282-129">Requirements</span></span>



| <span data-ttu-id="2b282-130">Требование</span><span class="sxs-lookup"><span data-stu-id="2b282-130">Requirement</span></span> | <span data-ttu-id="2b282-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2b282-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b282-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2b282-132">TAPI version</span></span><br/> | <span data-ttu-id="2b282-133">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="2b282-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="2b282-134">Header</span><span class="sxs-lookup"><span data-stu-id="2b282-134">Header</span></span><br/>       | <dl> <span data-ttu-id="2b282-135"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b282-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b282-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b282-136">Library</span></span><br/>      | <dl> <span data-ttu-id="2b282-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b282-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2b282-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2b282-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="2b282-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b282-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b282-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b282-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b282-141">**итаудиосеттингс**</span><span class="sxs-lookup"><span data-stu-id="2b282-141">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="2b282-142">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="2b282-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="2b282-143">**аудиосеттингспроперти**</span><span class="sxs-lookup"><span data-stu-id="2b282-143">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 





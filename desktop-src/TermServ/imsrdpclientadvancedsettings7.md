---
title: Интерфейс IMsRdpClientAdvancedSettings7
description: Предоставляет методы и свойства, управляющие дополнительными параметрами элемента управления ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672547"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="c11b5-105">Интерфейс IMsRdpClientAdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="c11b5-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="c11b5-106">Предоставляет методы и свойства, управляющие дополнительными параметрами элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c11b5-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="c11b5-107">Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="c11b5-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="c11b5-108">Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings7** в **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c11b5-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="c11b5-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="c11b5-109">Members</span></span>

<span data-ttu-id="c11b5-110">Интерфейс **IMsRdpClientAdvancedSettings7** наследует от **IMsRdpClientAdvancedSettings6**.</span><span class="sxs-lookup"><span data-stu-id="c11b5-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="c11b5-111">**IMsRdpClientAdvancedSettings7** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c11b5-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="c11b5-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c11b5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c11b5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c11b5-113">Properties</span></span>

<span data-ttu-id="c11b5-114">Интерфейс **IMsRdpClientAdvancedSettings7** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c11b5-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="c11b5-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="c11b5-115">Property</span></span>                                                                                                    | <span data-ttu-id="c11b5-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="c11b5-116">Access type</span></span>           | <span data-ttu-id="c11b5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c11b5-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c11b5-118">**аудиокаптурередиректионмоде**</span><span class="sxs-lookup"><span data-stu-id="c11b5-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="c11b5-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-119">Read/write</span></span><br/> | <span data-ttu-id="c11b5-120">Указывает или получает значение, указывающее, перенаправляется ли устройство ввода звука по умолчанию с клиента на удаленный сеанс.</span><span class="sxs-lookup"><span data-stu-id="c11b5-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="c11b5-121">**аудиокуалитимоде**</span><span class="sxs-lookup"><span data-stu-id="c11b5-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="c11b5-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-122">Read/write</span></span><br/> | <span data-ttu-id="c11b5-123">Указывает или получает значение, указывающее параметр режима качества звука для перенаправленного звука.</span><span class="sxs-lookup"><span data-stu-id="c11b5-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="c11b5-124">**енаблесуперпан**</span><span class="sxs-lookup"><span data-stu-id="c11b5-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="c11b5-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-125">Read/write</span></span><br/> | <span data-ttu-id="c11b5-126">Указывает или получает значение, указывающее, включен или отключен Суперпан.</span><span class="sxs-lookup"><span data-stu-id="c11b5-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="c11b5-127">**нетворкконнектионтипе**</span><span class="sxs-lookup"><span data-stu-id="c11b5-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="c11b5-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-128">Read/write</span></span><br/> | <span data-ttu-id="c11b5-129">Указывает или получает значение, указывающее тип сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="c11b5-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="c11b5-130">**редиректдиректкс**</span><span class="sxs-lookup"><span data-stu-id="c11b5-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="c11b5-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-131">Read/write</span></span><br/> | <span data-ttu-id="c11b5-132">Это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="c11b5-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="c11b5-133">**суперпанакцелератионфактор**</span><span class="sxs-lookup"><span data-stu-id="c11b5-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="c11b5-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-134">Read/write</span></span><br/> | <span data-ttu-id="c11b5-135">Указывает или получает значение, указывающее коэффициент ускорения Суперпан.</span><span class="sxs-lookup"><span data-stu-id="c11b5-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="c11b5-136">**видеоплайбаккмоде**</span><span class="sxs-lookup"><span data-stu-id="c11b5-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="c11b5-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c11b5-137">Read/write</span></span><br/> | <span data-ttu-id="c11b5-138">Указывает или получает значение, указывающее режим воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="c11b5-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="c11b5-139">Требования</span><span class="sxs-lookup"><span data-stu-id="c11b5-139">Requirements</span></span>



| <span data-ttu-id="c11b5-140">Требование</span><span class="sxs-lookup"><span data-stu-id="c11b5-140">Requirement</span></span> | <span data-ttu-id="c11b5-141">Значение</span><span class="sxs-lookup"><span data-stu-id="c11b5-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c11b5-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c11b5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c11b5-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c11b5-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="c11b5-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c11b5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c11b5-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c11b5-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="c11b5-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c11b5-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c11b5-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c11b5-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c11b5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c11b5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c11b5-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c11b5-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c11b5-150">IID</span><span class="sxs-lookup"><span data-stu-id="c11b5-150">IID</span></span><br/>                      | <span data-ttu-id="c11b5-151">IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="c11b5-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c11b5-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c11b5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c11b5-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c11b5-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c11b5-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c11b5-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c11b5-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c11b5-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c11b5-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c11b5-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="c11b5-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c11b5-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c11b5-158">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c11b5-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c11b5-159">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c11b5-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 


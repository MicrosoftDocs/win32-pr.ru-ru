---
description: Свойство PKEY \_ аудиоендпоинт \_ GUID предоставляет идентификатор устройства DirectSound, соответствующий устройству конечной точки аудио.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647147"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="6bab6-103">\_Идентификатор PKEY аудиоендпоинт \_</span><span class="sxs-lookup"><span data-stu-id="6bab6-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="6bab6-104">Свойство **PKEY \_ аудиоендпоинт \_ GUID** предоставляет идентификатор устройства DirectSound, соответствующий устройству конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="6bab6-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="6bab6-105">Значение свойства — это идентификатор GUID, который клиент может передать в качестве идентификатора устройства в функцию **директсаундкреате** или **Директсаундкаптурекреате** в API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="6bab6-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="6bab6-106">Это значение уникально определяет устройство звуковой конечной точки на всех устройствах аудио конечных точек в системе.</span><span class="sxs-lookup"><span data-stu-id="6bab6-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="6bab6-107">Дополнительные сведения о DirectSound см. в документации по пакету SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="6bab6-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="6bab6-108">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="6bab6-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="6bab6-109">Элемент **пвсзвал** структуры **пропвариант** указывает на строку расширенных символов, заканчивающуюся НУЛЕМ, которая содержит идентификатор GUID, определяющий устройство конечной точки звука в DirectSound.</span><span class="sxs-lookup"><span data-stu-id="6bab6-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="6bab6-110">Как упоминалось ранее, [API ммдевице](mmdevice-api.md) поддерживает [роли устройств](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6bab6-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="6bab6-111">Хотя DirectSound не поддерживает роли устройств напрямую, клиент DirectSound может использовать \_ свойство PKEY аудиоендпоинт GUID, \_ чтобы выбрать устройство для подготовки или записи DirectSound на основе роли устройства.</span><span class="sxs-lookup"><span data-stu-id="6bab6-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="6bab6-112">Например, приложение DirectSound выполняет следующие действия, чтобы создать устройство DirectSound, соответствующее устройству конечной точки отрисовки, к которому пользователь назначил роль Емултимедиа:</span><span class="sxs-lookup"><span data-stu-id="6bab6-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="6bab6-113">Вызовите метод [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства конечной точки отрисовки с ролью емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="6bab6-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="6bab6-114">Вызовите метод [**иммдевице:: опенпропертисторе**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) , чтобы получить интерфейс **ипропертисторе** устройства емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="6bab6-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="6bab6-115">Дополнительные сведения о **ипропертисторе** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6bab6-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="6bab6-116">Вызовите метод **ипропертисторе:: GetValue** , чтобы получить \_ \_ значение свойства аудиоендпоинт GUID PKEY.</span><span class="sxs-lookup"><span data-stu-id="6bab6-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="6bab6-117">Преобразование значения свойства из GUID в строковом формате в 16-байтовую структуру GUID.</span><span class="sxs-lookup"><span data-stu-id="6bab6-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="6bab6-118">Вызовите функцию **директсаундкреате** с идентификатором GUID, чтобы создать устройство с ролью емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="6bab6-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="6bab6-119">**PKEY \_ Аудиоендпоинт \_ GUID** — это свойство, доступное только для чтения, независимо от режима доступа к хранилищу, запрошенного приложением в [**Иммдевице:: опенпропертисторе**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span><span class="sxs-lookup"><span data-stu-id="6bab6-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="6bab6-120">Если приложение пытается установить значение с помощью **ипропертисторе:: SetValue**, этот вызов завершается с \_ кодом ошибки E ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="6bab6-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="6bab6-121">Обратите внимание, что 16-байтовый GUID, созданный на шаге 4, соответствует идентификатору GUID устройства, идентифицирующему устройство при перечислении устройств DirectSound.</span><span class="sxs-lookup"><span data-stu-id="6bab6-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="6bab6-122">Функция **директсаунденумерате** перечисляет устройства конечных точек, а функция **директсаундкаптуринумерате** перечисляет устройства конечных точек.</span><span class="sxs-lookup"><span data-stu-id="6bab6-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="6bab6-123">В любом случае идентификатор GUID устройства — это первый параметр, передаваемый функции обратного вызова перечисления.</span><span class="sxs-lookup"><span data-stu-id="6bab6-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="6bab6-124">Дополнительные сведения о перечислении DirectSound см. в документации по пакету SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="6bab6-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="6bab6-125">Пример кода, в котором используется свойство PKEY \_ аудиоендпоинт \_ GUID, см. в разделе [роли устройств для приложений DirectSound](device-roles-for-directsound-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6bab6-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bab6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6bab6-126">Requirements</span></span>



| <span data-ttu-id="6bab6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6bab6-127">Requirement</span></span> | <span data-ttu-id="6bab6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6bab6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bab6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bab6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6bab6-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bab6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6bab6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bab6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6bab6-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6bab6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6bab6-133">Header</span><span class="sxs-lookup"><span data-stu-id="6bab6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bab6-134"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bab6-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bab6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bab6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bab6-136">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="6bab6-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="6bab6-137">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="6bab6-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 





---
description: Указывает, какие звуковые устройства использует DSP для записи и визуализации звука.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Свойство MFPKEY_WMAAECMA_DEVICE_INDEXES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898206"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="fd157-103">\_ \_ \_ Свойство индексов устройства мфпкэй вмааекма</span><span class="sxs-lookup"><span data-stu-id="fd157-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="fd157-104">Указывает, какие звуковые устройства использует DSP для записи и визуализации звука.</span><span class="sxs-lookup"><span data-stu-id="fd157-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fd157-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="fd157-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fd157-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="fd157-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="fd157-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fd157-107">Data Type</span></span>

<span data-ttu-id="fd157-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fd157-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="fd157-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd157-109">Default Value</span></span>

<span data-ttu-id="fd157-110">(-1,-1).</span><span class="sxs-lookup"><span data-stu-id="fd157-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fd157-111">Применение</span><span class="sxs-lookup"><span data-stu-id="fd157-111">Applies To</span></span>

-   [<span data-ttu-id="fd157-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="fd157-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="fd157-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd157-113">Remarks</span></span>

<span data-ttu-id="fd157-114">Задайте это свойство при использовании DSP в режиме исходного кода.</span><span class="sxs-lookup"><span data-stu-id="fd157-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="fd157-115">DSP игнорирует это свойство в режиме фильтрации.</span><span class="sxs-lookup"><span data-stu-id="fd157-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="fd157-116">Значение свойства — 2 16-разрядное **слово**, упакованное в **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="fd157-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="fd157-117">Верхние 16 бит указывают устройство отрисовки звука (обычно это докладчик), а младшие 16 бит указывают устройство записи (обычно это микрофон).</span><span class="sxs-lookup"><span data-stu-id="fd157-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="fd157-118">Каждое устройство указывается в виде индекса в коллекции звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="fd157-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="fd157-119">Если индекс равен-1, используется устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fd157-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="fd157-120">Индекс устройства соответствует индексу коллекции, используемому в интерфейсе [**иммдевицеколлектион**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) .</span><span class="sxs-lookup"><span data-stu-id="fd157-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="fd157-121">Приложение должно воспроизводить высокопроизводительный Voice через выбранное устройство рендеринга.</span><span class="sxs-lookup"><span data-stu-id="fd157-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="fd157-122">(В конце концов, это голосовая связь пользователя на другом конце телефонной линии, которая воспроизводится на компьютере пользователя.) Если выбранное устройство отрисовки не имеет активного потока, то DSP не сможет обработать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="fd157-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="fd157-123">Значение этого свойства по умолчанию равно (-1,-1).</span><span class="sxs-lookup"><span data-stu-id="fd157-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="fd157-124">В следующем примере показано, как инициализировать **пропвариант** для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="fd157-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="fd157-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fd157-125">Requirements</span></span>



| <span data-ttu-id="fd157-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fd157-126">Requirement</span></span> | <span data-ttu-id="fd157-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fd157-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd157-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd157-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fd157-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd157-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd157-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd157-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fd157-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd157-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd157-132">Header</span><span class="sxs-lookup"><span data-stu-id="fd157-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd157-133"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd157-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd157-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd157-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd157-135">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd157-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fd157-136">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="fd157-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 

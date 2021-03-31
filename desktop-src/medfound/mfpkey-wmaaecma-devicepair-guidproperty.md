---
description: Определяет комбинацию звуковых устройств, которые в настоящее время использует приложение, с помощью схемы DSP для записи голоса.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: Свойство MFPKEY_WMAAECMA_DEVICEPAIR_GUID (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155391"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="97268-103">МФПКЭЙ \_ вмааекма \_ Девицепаир, \_ свойство GUID</span><span class="sxs-lookup"><span data-stu-id="97268-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="97268-104">Определяет комбинацию звуковых устройств, которые в настоящее время использует приложение, с помощью схемы DSP для записи голоса.</span><span class="sxs-lookup"><span data-stu-id="97268-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="97268-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="97268-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="97268-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="97268-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="97268-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="97268-107">Data Type</span></span>

<span data-ttu-id="97268-108">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="97268-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="97268-109">Применение</span><span class="sxs-lookup"><span data-stu-id="97268-109">Applies To</span></span>

-   [<span data-ttu-id="97268-110">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="97268-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="97268-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97268-111">Remarks</span></span>

<span data-ttu-id="97268-112">Задайте это свойство, если вы используете DSP в режиме фильтрации, а значение свойства [мфпкэй вмааекма " \_ \_ получить \_ \_ статистику TS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) " является вариантным \_ true.</span><span class="sxs-lookup"><span data-stu-id="97268-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="97268-113">Если свойство [**мфпкэй \_ вмааекма \_ Получение \_ \_ статистики TS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) имеет \_ значение true, то DSP собирает статистику о метках времени на звуковых устройствах и сохраняет эти сведения в реестре.</span><span class="sxs-lookup"><span data-stu-id="97268-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="97268-114">Эти статистические данные могут изменяться для каждого сочетания устройства аудиозаписи и устройства воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="97268-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="97268-115">Поэтому приложение должно назначить идентификатор GUID для распознавания конкретного сочетания используемых устройств.</span><span class="sxs-lookup"><span data-stu-id="97268-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="97268-116">Приложение должно отследить этот GUID, чтобы он мог назначить тот же идентификатор GUID при использовании той же пары звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="97268-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="97268-117">Если вы используете DSP в исходном режиме, не нужно задавать это свойство.</span><span class="sxs-lookup"><span data-stu-id="97268-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="97268-118">DSP автоматически создает идентификатор GUID на основе значения свойства [мфпкэй \_ вмааекма \_ Device \_ indexes](mfpkey-wmaaecma-device-indexesproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="97268-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="97268-119">Требования</span><span class="sxs-lookup"><span data-stu-id="97268-119">Requirements</span></span>



| <span data-ttu-id="97268-120">Требование</span><span class="sxs-lookup"><span data-stu-id="97268-120">Requirement</span></span> | <span data-ttu-id="97268-121">Значение</span><span class="sxs-lookup"><span data-stu-id="97268-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97268-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97268-122">Minimum supported client</span></span><br/> | <span data-ttu-id="97268-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97268-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="97268-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97268-124">Minimum supported server</span></span><br/> | <span data-ttu-id="97268-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97268-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97268-126">Header</span><span class="sxs-lookup"><span data-stu-id="97268-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="97268-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="97268-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97268-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97268-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97268-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97268-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="97268-130">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="97268-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 

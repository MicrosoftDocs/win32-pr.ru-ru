---
description: Указывает, хранится ли в реестре DSP для записи речи статистика по метке времени.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Свойство MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692596"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="77804-103">МФПКЭЙ \_ вмааекма \_ Получение \_ \_ Свойства статистики TS</span><span class="sxs-lookup"><span data-stu-id="77804-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="77804-104">Указывает, хранится ли в реестре DSP для записи речи статистика по метке времени.</span><span class="sxs-lookup"><span data-stu-id="77804-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="77804-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="77804-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="77804-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="77804-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="77804-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="77804-107">Data Type</span></span>

<span data-ttu-id="77804-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="77804-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="77804-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="77804-109">Default Value</span></span>

<span data-ttu-id="77804-110">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="77804-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="77804-111">Применение</span><span class="sxs-lookup"><span data-stu-id="77804-111">Applies To</span></span>

-   [<span data-ttu-id="77804-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="77804-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="77804-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77804-113">Remarks</span></span>

<span data-ttu-id="77804-114">Алгоритмы отмены акустического эха (AEC) зависят от точных меток времени в звуковых потоках.</span><span class="sxs-lookup"><span data-stu-id="77804-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="77804-115">На практике метки времени часто неидеальныы, а различные звуковые устройства могут демонстрировать различные тарифы и отклонения.</span><span class="sxs-lookup"><span data-stu-id="77804-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="77804-116">Если параметр AEC включен, DSP собирает статистические данные о метках времени и использует эти сведения для компенсации неточностей.</span><span class="sxs-lookup"><span data-stu-id="77804-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="77804-117">Если значение этого свойства равно \_ true, то DSP сохраняет статистические данные, собираемые в реестре.</span><span class="sxs-lookup"><span data-stu-id="77804-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="77804-118">В следующий раз, когда DSP выполняет контекст AEC, используя ту же пару звуковых устройств, он считывает статистические данные из реестра, что позволяет поставщику схемы эффективности работать более эффективно.</span><span class="sxs-lookup"><span data-stu-id="77804-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="77804-119">Если для этого свойства задать значение \_ true и вы используете DSP в режиме фильтрации, необходимо также задать свойство [мфпкэй \_ вмааекма \_ девицепаир \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="77804-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="77804-120">В режиме исходного кода это необязательно.</span><span class="sxs-lookup"><span data-stu-id="77804-120">In source mode, this is not required.</span></span>

<span data-ttu-id="77804-121">Значение этого свойства по умолчанию — VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="77804-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="77804-122">DSP использует это свойство только в том случае, если включена обработка AEC.</span><span class="sxs-lookup"><span data-stu-id="77804-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="77804-123">Требования</span><span class="sxs-lookup"><span data-stu-id="77804-123">Requirements</span></span>



| <span data-ttu-id="77804-124">Требование</span><span class="sxs-lookup"><span data-stu-id="77804-124">Requirement</span></span> | <span data-ttu-id="77804-125">Значение</span><span class="sxs-lookup"><span data-stu-id="77804-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77804-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77804-126">Minimum supported client</span></span><br/> | <span data-ttu-id="77804-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77804-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77804-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77804-128">Minimum supported server</span></span><br/> | <span data-ttu-id="77804-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77804-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77804-130">Header</span><span class="sxs-lookup"><span data-stu-id="77804-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="77804-131"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="77804-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77804-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77804-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77804-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77804-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="77804-134">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="77804-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 

---
description: Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: Свойство MFPKEY_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991597"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="cc895-103">МФПКЭЙ \_ вбркуалити, свойство</span><span class="sxs-lookup"><span data-stu-id="cc895-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="cc895-104">Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).</span><span class="sxs-lookup"><span data-stu-id="cc895-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cc895-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="cc895-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cc895-106">g \_ всзвмвквбркуалити, g \_ всзвмкпаудиовбркуалити</span><span class="sxs-lookup"><span data-stu-id="cc895-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="cc895-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc895-107">Data Type</span></span>

<span data-ttu-id="cc895-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cc895-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="cc895-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc895-109">Remarks</span></span>

<span data-ttu-id="cc895-110">Не все значения в диапазоне имеют уникальное значение.</span><span class="sxs-lookup"><span data-stu-id="cc895-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="cc895-111">Значения, представляющие этап качества, начиная с предыдущего уровня: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 и 100.</span><span class="sxs-lookup"><span data-stu-id="cc895-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="cc895-112">Для объектов звукового кодировщика режимы качества предоставляются в структуре [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) типов выходных данных, получаемых с помощью [**Имедиаобжект:: жетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="cc895-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc895-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cc895-113">Requirements</span></span>



| <span data-ttu-id="cc895-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cc895-114">Requirement</span></span> | <span data-ttu-id="cc895-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cc895-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc895-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc895-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cc895-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc895-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cc895-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc895-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cc895-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc895-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc895-120">Header</span><span class="sxs-lookup"><span data-stu-id="cc895-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc895-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc895-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc895-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc895-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc895-123">Перечисление типов аудио для конкретных режимов кодирования</span><span class="sxs-lookup"><span data-stu-id="cc895-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="cc895-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc895-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

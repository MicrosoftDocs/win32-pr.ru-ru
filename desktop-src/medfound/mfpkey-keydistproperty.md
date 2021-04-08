---
description: Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Свойство MFPKEY_KEYDIST (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908771"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="59caa-103">МФПКЭЙ \_ кэйдист, свойство</span><span class="sxs-lookup"><span data-stu-id="59caa-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="59caa-104">Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.</span><span class="sxs-lookup"><span data-stu-id="59caa-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="59caa-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="59caa-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="59caa-106">g \_ всзвмвккэйфрамедистанце</span><span class="sxs-lookup"><span data-stu-id="59caa-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="59caa-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="59caa-107">Data Type</span></span>

<span data-ttu-id="59caa-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="59caa-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="59caa-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="59caa-109">Default Value</span></span>

<span data-ttu-id="59caa-110">Значение по умолчанию зависит от того, какая версия Windows выполняется, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="59caa-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="59caa-111">Операционная система</span><span class="sxs-lookup"><span data-stu-id="59caa-111">Operating system</span></span> | <span data-ttu-id="59caa-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="59caa-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="59caa-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="59caa-113">Windows XP</span></span>       | <span data-ttu-id="59caa-114">8000</span><span class="sxs-lookup"><span data-stu-id="59caa-114">8000</span></span>          |
| <span data-ttu-id="59caa-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59caa-115">Windows Vista</span></span>    | <span data-ttu-id="59caa-116">8000</span><span class="sxs-lookup"><span data-stu-id="59caa-116">8000</span></span>          |
| <span data-ttu-id="59caa-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59caa-117">Windows 7</span></span>        | <span data-ttu-id="59caa-118">2000</span><span class="sxs-lookup"><span data-stu-id="59caa-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="59caa-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59caa-119">Remarks</span></span>

<span data-ttu-id="59caa-120">Внутренняя логика кодека определяет фактическое расположение каждого ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="59caa-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="59caa-121">Расстояние между любыми двумя ключевыми кадрами может быть меньше значения этого свойства, однако оно никогда не будет больше.</span><span class="sxs-lookup"><span data-stu-id="59caa-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="59caa-122">Требования</span><span class="sxs-lookup"><span data-stu-id="59caa-122">Requirements</span></span>



| <span data-ttu-id="59caa-123">Требование</span><span class="sxs-lookup"><span data-stu-id="59caa-123">Requirement</span></span> | <span data-ttu-id="59caa-124">Значение</span><span class="sxs-lookup"><span data-stu-id="59caa-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59caa-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59caa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59caa-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="59caa-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="59caa-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59caa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59caa-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59caa-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59caa-129">Header</span><span class="sxs-lookup"><span data-stu-id="59caa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="59caa-130"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="59caa-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59caa-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59caa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59caa-132">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59caa-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





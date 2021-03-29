---
description: Задает числовое представление компромисса между плавностью движения и качеством изображения для вывода кодека.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Свойство MFPKEY_CRISP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812766"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="399b8-103">\_Четкое свойство мфпкэй</span><span class="sxs-lookup"><span data-stu-id="399b8-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="399b8-104">Задает числовое представление компромисса между плавностью движения и качеством изображения для вывода кодека.</span><span class="sxs-lookup"><span data-stu-id="399b8-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="399b8-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="399b8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="399b8-106">g \_ всзвмвккрисп</span><span class="sxs-lookup"><span data-stu-id="399b8-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="399b8-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="399b8-107">Data Type</span></span>

<span data-ttu-id="399b8-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="399b8-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="399b8-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="399b8-109">Default Value</span></span>

<span data-ttu-id="399b8-110">75</span><span class="sxs-lookup"><span data-stu-id="399b8-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="399b8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="399b8-111">Remarks</span></span>

<span data-ttu-id="399b8-112">Это целое значение может находиться в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="399b8-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="399b8-113">Чем выше значение, тем больше кодек будет оптимизировать кодирование для качества изображения отдельных кадров, что обычно сокращает гладкость движения.</span><span class="sxs-lookup"><span data-stu-id="399b8-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="399b8-114">Это свойство должно быть задано только для кодирования с постоянной битовой скоростью (CBR).</span><span class="sxs-lookup"><span data-stu-id="399b8-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="399b8-115">Оптимизация для кодирования с переменной скоростью (VBR) работает по-разному.</span><span class="sxs-lookup"><span data-stu-id="399b8-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="399b8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="399b8-116">Requirements</span></span>



| <span data-ttu-id="399b8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="399b8-117">Requirement</span></span> | <span data-ttu-id="399b8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="399b8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="399b8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="399b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="399b8-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="399b8-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="399b8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="399b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="399b8-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="399b8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="399b8-123">Header</span><span class="sxs-lookup"><span data-stu-id="399b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="399b8-124"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="399b8-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="399b8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="399b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399b8-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="399b8-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





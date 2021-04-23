---
description: Корректирует контрастность.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: Свойство MFPKEY_COLOR_CONTRAST (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711787"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="b3b9a-103">\_ \_ Свойство контрастности цвета мфпкэй</span><span class="sxs-lookup"><span data-stu-id="b3b9a-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="b3b9a-104">Корректирует контрастность.</span><span class="sxs-lookup"><span data-stu-id="b3b9a-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b3b9a-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="b3b9a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b3b9a-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b3b9a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b3b9a-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b3b9a-107">Data Type</span></span>

<span data-ttu-id="b3b9a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b3b9a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b3b9a-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b3b9a-109">Default Value</span></span>

<span data-ttu-id="b3b9a-110">0</span><span class="sxs-lookup"><span data-stu-id="b3b9a-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="b3b9a-111">Применение</span><span class="sxs-lookup"><span data-stu-id="b3b9a-111">Applies To</span></span>

-   [<span data-ttu-id="b3b9a-112">Преобразование элемента управления цветом DSP</span><span class="sxs-lookup"><span data-stu-id="b3b9a-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="b3b9a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3b9a-113">Remarks</span></span>

<span data-ttu-id="b3b9a-114">Корректировка контрастности выполняется путем умножения значений Икбкр на коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b3b9a-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="b3b9a-115">Это свойство имеет диапазон от-127 до 127.</span><span class="sxs-lookup"><span data-stu-id="b3b9a-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="b3b9a-116">Ноль означает отсутствие изменений в контрасте.</span><span class="sxs-lookup"><span data-stu-id="b3b9a-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b9a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b3b9a-117">Requirements</span></span>



| <span data-ttu-id="b3b9a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b3b9a-118">Requirement</span></span> | <span data-ttu-id="b3b9a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b3b9a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b9a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3b9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b9a-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3b9a-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b3b9a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3b9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b9a-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3b9a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3b9a-124">Header</span><span class="sxs-lookup"><span data-stu-id="b3b9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b9a-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b9a-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3b9a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3b9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b9a-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3b9a-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

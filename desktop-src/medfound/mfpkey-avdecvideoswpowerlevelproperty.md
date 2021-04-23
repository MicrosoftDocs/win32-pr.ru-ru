---
description: Задает уровень питания для декодера.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Свойство MFPKEY_AVDecVideoSWPowerLevel (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692502"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="b472e-103">МФПКЭЙ \_ авдеквидеосвповерлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="b472e-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="b472e-104">Задает уровень питания для декодера.</span><span class="sxs-lookup"><span data-stu-id="b472e-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b472e-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="b472e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b472e-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b472e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b472e-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b472e-107">Data Type</span></span>

<span data-ttu-id="b472e-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b472e-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="b472e-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b472e-109">Default Value</span></span>

<span data-ttu-id="b472e-110">**100**</span><span class="sxs-lookup"><span data-stu-id="b472e-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="b472e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b472e-111">Remarks</span></span>

<span data-ttu-id="b472e-112">Для этого свойства необходимо задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b472e-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="b472e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b472e-113">Value</span></span> | <span data-ttu-id="b472e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b472e-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="b472e-115">0</span><span class="sxs-lookup"><span data-stu-id="b472e-115">0</span></span>     | <span data-ttu-id="b472e-116">Декодер использует уровень питания, оптимизированный для времени работы батареи.</span><span class="sxs-lookup"><span data-stu-id="b472e-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="b472e-117">50</span><span class="sxs-lookup"><span data-stu-id="b472e-117">50</span></span>    | <span data-ttu-id="b472e-118">Декодер использует сбалансированный уровень электропитания.</span><span class="sxs-lookup"><span data-stu-id="b472e-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="b472e-119">100</span><span class="sxs-lookup"><span data-stu-id="b472e-119">100</span></span>   | <span data-ttu-id="b472e-120">Декодер использует уровень питания, оптимизированный для качества видео.</span><span class="sxs-lookup"><span data-stu-id="b472e-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b472e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b472e-121">Requirements</span></span>



| <span data-ttu-id="b472e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b472e-122">Requirement</span></span> | <span data-ttu-id="b472e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b472e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b472e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b472e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b472e-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b472e-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b472e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b472e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b472e-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b472e-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b472e-128">Header</span><span class="sxs-lookup"><span data-stu-id="b472e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b472e-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b472e-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b472e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b472e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b472e-131">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b472e-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

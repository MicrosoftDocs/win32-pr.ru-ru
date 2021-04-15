---
title: Сообщение BCM_GETIDEALSIZE (Коммктрл. h)
description: Возвращает размер кнопки, которая лучше подходит для текста и изображения, если имеется список изображений. Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки жетидеалсизе.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Элементы управления Windows для BCM_GETIDEALSIZE сообщений
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654489"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="ba4bf-105">\_Сообщение ЖЕТИДЕАЛСИЗЕ BCM</span><span class="sxs-lookup"><span data-stu-id="ba4bf-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="ba4bf-106">Возвращает размер кнопки, которая лучше подходит для текста и изображения, если имеется список изображений.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="ba4bf-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ жетидеалсизе**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="ba4bf-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba4bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba4bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba4bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4bf-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba4bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba4bf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4bf-112">Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) , которая получает требуемый размер кнопки, включая текст и список изображений, если они есть.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="ba4bf-113">Вызывающее приложение отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="ba4bf-114">Задайте нулевые значения для элементов **CX** и **CY** , чтобы они имели идеальную высоту и ширину, возвращаемые в структуре **размера** .</span><span class="sxs-lookup"><span data-stu-id="ba4bf-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="ba4bf-115">Чтобы задать ширину кнопки, задайте для элемента **CX** ширину требуемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="ba4bf-116">Система будет рассчитывать идеальную высоту для этой ширины и возвращать ее в элемент **CY** .</span><span class="sxs-lookup"><span data-stu-id="ba4bf-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba4bf-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba4bf-117">Return value</span></span>

<span data-ttu-id="ba4bf-118">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="ba4bf-119">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba4bf-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba4bf-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba4bf-121">Если ширина специальной кнопки не нужна, необходимо задать оба элемента [**size**](/previous-versions//dd145106(v=vs.85)) равным нулю, чтобы вычислить и вернуть идеальную высоту и ширину.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="ba4bf-122">Если значение элемента **CX** больше нуля, то это значение считается требуемой шириной кнопки, а идеальная высота для этой ширины вычисляется и возвращается в элемент **CY** .</span><span class="sxs-lookup"><span data-stu-id="ba4bf-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="ba4bf-123">Это сообщение наиболее применимо к кнопкам.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="ba4bf-124">Когда отправляется на кнопку, сообщение получает ограничивающий прямоугольник, необходимый для вывода текста кнопки.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="ba4bf-125">Кроме того, если у кнопки есть список изображений, ограничивающий прямоугольник также будет иметь размер, чтобы включить изображение кнопки.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="ba4bf-126">При отправке на кнопку любого другого типа извлекается размер прямоугольника окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="ba4bf-127">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="ba4bf-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ba4bf-128">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba4bf-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba4bf-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ba4bf-129">Requirements</span></span>



| <span data-ttu-id="ba4bf-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ba4bf-130">Requirement</span></span> | <span data-ttu-id="ba4bf-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ba4bf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4bf-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba4bf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ba4bf-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba4bf-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba4bf-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba4bf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ba4bf-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba4bf-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba4bf-136">Header</span><span class="sxs-lookup"><span data-stu-id="ba4bf-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba4bf-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba4bf-137"><dt>Commctrl.h</dt></span></span> </dl> |



 


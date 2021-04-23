---
title: IMsRdpClientAdvancedSettings7 Суперпанакцелератионфактор, свойство
description: Указывает или получает значение, указывающее коэффициент ускорения Суперпан. Коэффициент ускорения Суперпан определяет скорость движения экрана в режиме Суперпан.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Суперпанакцелератионфактор
- Службы удаленных рабочих столов свойства Суперпанакцелератионфактор, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Суперпанакцелератионфактор
- Службы удаленных рабочих столов свойства Суперпанакцелератионфактор, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Суперпанакцелератионфактор
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989414"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="4aaac-109">Свойство IMsRdpClientAdvancedSettings7:: Суперпанакцелератионфактор</span><span class="sxs-lookup"><span data-stu-id="4aaac-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="4aaac-110">Указывает или получает значение, указывающее коэффициент ускорения Суперпан.</span><span class="sxs-lookup"><span data-stu-id="4aaac-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="4aaac-111">Коэффициент ускорения Суперпан определяет скорость движения экрана в режиме Суперпан.</span><span class="sxs-lookup"><span data-stu-id="4aaac-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="4aaac-112">Коэффициент ускорения — это число пикселей, которое прокручивается на экране в заданном направлении для каждого пикселя движения мыши клиентом.</span><span class="sxs-lookup"><span data-stu-id="4aaac-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="4aaac-113">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4aaac-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aaac-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aaac-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="4aaac-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4aaac-115">Property value</span></span>

<span data-ttu-id="4aaac-116">Устанавливаемый коэффициент ускорения Суперпан.</span><span class="sxs-lookup"><span data-stu-id="4aaac-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="4aaac-117">Коэффициент ускорения Суперпан — это число пикселей, которое экранное представление прокручивается в заданном направлении для каждого пикселя движения мыши.</span><span class="sxs-lookup"><span data-stu-id="4aaac-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aaac-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aaac-118">Remarks</span></span>

<span data-ttu-id="4aaac-119">Дополнительные сведения о Суперпан см. в разделе [**енаблесуперпан**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span><span class="sxs-lookup"><span data-stu-id="4aaac-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aaac-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4aaac-120">Requirements</span></span>



| <span data-ttu-id="4aaac-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4aaac-121">Requirement</span></span> | <span data-ttu-id="4aaac-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4aaac-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aaac-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4aaac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4aaac-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4aaac-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="4aaac-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4aaac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4aaac-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4aaac-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="4aaac-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4aaac-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="4aaac-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aaac-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4aaac-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4aaac-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aaac-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aaac-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4aaac-131">IID</span><span class="sxs-lookup"><span data-stu-id="4aaac-131">IID</span></span><br/>                      | <span data-ttu-id="4aaac-132">IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="4aaac-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4aaac-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aaac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aaac-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4aaac-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4aaac-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4aaac-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4aaac-136">**енаблесуперпан**</span><span class="sxs-lookup"><span data-stu-id="4aaac-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 






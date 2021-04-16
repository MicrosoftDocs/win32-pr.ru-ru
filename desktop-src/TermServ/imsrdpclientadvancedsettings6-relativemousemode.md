---
title: IMsRdpClientAdvancedSettings6 Релативемаусемоде, свойство
description: Указывает, следует ли использовать относительный режим для мыши.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Релативемаусемоде
- Службы удаленных рабочих столов свойства Релативемаусемоде, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Релативемаусемоде
- Службы удаленных рабочих столов свойства Релативемаусемоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Релативемаусемоде
- Службы удаленных рабочих столов свойства Релативемаусемоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Релативемаусемоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672729"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="7a288-110">Свойство IMsRdpClientAdvancedSettings6:: Релативемаусемоде</span><span class="sxs-lookup"><span data-stu-id="7a288-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="7a288-111">Указывает, следует ли использовать относительный режим для мыши.</span><span class="sxs-lookup"><span data-stu-id="7a288-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="7a288-112">Содержит **вариант \_ true** , если мышь находится в относительном режиме, или **вариант \_ false** , если мышь находится в абсолютном режиме.</span><span class="sxs-lookup"><span data-stu-id="7a288-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="7a288-113">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7a288-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a288-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a288-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="7a288-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7a288-115">Property value</span></span>

<span data-ttu-id="7a288-116">Содержит новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7a288-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a288-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a288-117">Remarks</span></span>

<span data-ttu-id="7a288-118">Режим мыши показывает, как элемент управления ActiveX вычисляет координаты мыши, которые она отправляет на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="7a288-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="7a288-119">Когда указатель мыши находится в относительном режиме, элемент управления ActiveX вычисляет координаты мыши относительно последней положения мыши.</span><span class="sxs-lookup"><span data-stu-id="7a288-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="7a288-120">Когда мышь находится в абсолютном режиме, элемент управления ActiveX вычисляет координаты мыши относительно рабочего стола сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7a288-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a288-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7a288-121">Requirements</span></span>



| <span data-ttu-id="7a288-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7a288-122">Requirement</span></span> | <span data-ttu-id="7a288-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7a288-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a288-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a288-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7a288-125">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7a288-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="7a288-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a288-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7a288-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a288-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7a288-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7a288-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a288-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a288-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7a288-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a288-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a288-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a288-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7a288-132">IID</span><span class="sxs-lookup"><span data-stu-id="7a288-132">IID</span></span><br/>                      | <span data-ttu-id="7a288-133">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="7a288-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a288-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a288-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a288-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7a288-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7a288-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7a288-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7a288-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7a288-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 






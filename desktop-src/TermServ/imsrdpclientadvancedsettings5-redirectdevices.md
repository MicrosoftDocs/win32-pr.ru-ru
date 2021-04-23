---
title: IMsRdpClientAdvancedSettings5 Редиректдевицес, свойство
description: Задает или получает конфигурацию для перенаправления устройства.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректдевицес
- Службы удаленных рабочих столов свойства Редиректдевицес, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректдевицес
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672573"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="cae41-112">Свойство IMsRdpClientAdvancedSettings5:: Редиректдевицес</span><span class="sxs-lookup"><span data-stu-id="cae41-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="cae41-113">Задает или получает конфигурацию для перенаправления устройства.</span><span class="sxs-lookup"><span data-stu-id="cae41-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="cae41-114">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cae41-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae41-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cae41-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="cae41-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cae41-116">Property value</span></span>

<span data-ttu-id="cae41-117">Задает для режима перенаправления устройства **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="cae41-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="cae41-118">Если задано **значение true**, режим перенаправления устройств включен.</span><span class="sxs-lookup"><span data-stu-id="cae41-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae41-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cae41-119">Requirements</span></span>



| <span data-ttu-id="cae41-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cae41-120">Requirement</span></span> | <span data-ttu-id="cae41-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cae41-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae41-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cae41-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cae41-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cae41-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="cae41-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cae41-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cae41-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cae41-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="cae41-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cae41-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="cae41-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae41-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cae41-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cae41-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae41-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae41-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cae41-130">IID</span><span class="sxs-lookup"><span data-stu-id="cae41-130">IID</span></span><br/>                      | <span data-ttu-id="cae41-131">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="cae41-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cae41-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cae41-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae41-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="cae41-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="cae41-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="cae41-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="cae41-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="cae41-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="cae41-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="cae41-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 






---
title: IMsRdpClientAdvancedSettings5 Редиректпосдевицес, свойство
description: Задает или получает конфигурацию для перенаправления устройства точки обслуживания.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректпосдевицес
- Службы удаленных рабочих столов свойства Редиректпосдевицес, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректпосдевицес
- Службы удаленных рабочих столов свойства Редиректпосдевицес, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректпосдевицес
- Службы удаленных рабочих столов свойства Редиректпосдевицес, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректпосдевицес
- Службы удаленных рабочих столов свойства Редиректпосдевицес, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректпосдевицес
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136530"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="45539-112">Свойство IMsRdpClientAdvancedSettings5:: Редиректпосдевицес</span><span class="sxs-lookup"><span data-stu-id="45539-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="45539-113">Задает или получает конфигурацию для перенаправления устройства точки обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45539-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="45539-114">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="45539-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="45539-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45539-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="45539-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="45539-116">Property value</span></span>

<span data-ttu-id="45539-117">Устанавливает режим перенаправления устройства точки обслуживания в **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="45539-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="45539-118">Если задано значение **true**, то включен режим перенаправления устройства точки обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45539-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="45539-119">Требования</span><span class="sxs-lookup"><span data-stu-id="45539-119">Requirements</span></span>



| <span data-ttu-id="45539-120">Требование</span><span class="sxs-lookup"><span data-stu-id="45539-120">Requirement</span></span> | <span data-ttu-id="45539-121">Значение</span><span class="sxs-lookup"><span data-stu-id="45539-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45539-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45539-122">Minimum supported client</span></span><br/> | <span data-ttu-id="45539-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45539-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="45539-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45539-124">Minimum supported server</span></span><br/> | <span data-ttu-id="45539-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45539-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="45539-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="45539-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="45539-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45539-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="45539-128">DLL</span><span class="sxs-lookup"><span data-stu-id="45539-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45539-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45539-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="45539-130">IID</span><span class="sxs-lookup"><span data-stu-id="45539-130">IID</span></span><br/>                      | <span data-ttu-id="45539-131">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="45539-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45539-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45539-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45539-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="45539-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="45539-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="45539-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="45539-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="45539-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="45539-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="45539-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 






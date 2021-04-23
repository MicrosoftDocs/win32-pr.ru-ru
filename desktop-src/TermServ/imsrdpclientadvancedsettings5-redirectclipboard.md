---
title: IMsRdpClientAdvancedSettings5 Редиректклипбоард, свойство
description: Задает или получает конфигурацию для перенаправления буфера обмена.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректклипбоард
- Службы удаленных рабочих столов свойства Редиректклипбоард, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректклипбоард
- Службы удаленных рабочих столов свойства Редиректклипбоард, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректклипбоард
- Службы удаленных рабочих столов свойства Редиректклипбоард, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректклипбоард
- Службы удаленных рабочих столов свойства Редиректклипбоард, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректклипбоард
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988406"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="35846-112">Свойство IMsRdpClientAdvancedSettings5:: Редиректклипбоард</span><span class="sxs-lookup"><span data-stu-id="35846-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="35846-113">Задает или получает конфигурацию для перенаправления буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="35846-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="35846-114">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="35846-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35846-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35846-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="35846-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="35846-116">Property value</span></span>

<span data-ttu-id="35846-117">Задает для режима перенаправления буфера обмена **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="35846-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="35846-118">Если задано значение **true**, то включен режим перенаправления буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="35846-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="35846-119">Требования</span><span class="sxs-lookup"><span data-stu-id="35846-119">Requirements</span></span>



| <span data-ttu-id="35846-120">Требование</span><span class="sxs-lookup"><span data-stu-id="35846-120">Requirement</span></span> | <span data-ttu-id="35846-121">Значение</span><span class="sxs-lookup"><span data-stu-id="35846-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35846-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35846-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35846-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35846-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="35846-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35846-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35846-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35846-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="35846-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="35846-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="35846-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35846-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="35846-128">DLL</span><span class="sxs-lookup"><span data-stu-id="35846-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35846-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35846-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="35846-130">IID</span><span class="sxs-lookup"><span data-stu-id="35846-130">IID</span></span><br/>                      | <span data-ttu-id="35846-131">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="35846-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35846-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35846-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35846-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="35846-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="35846-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="35846-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="35846-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="35846-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="35846-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="35846-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 






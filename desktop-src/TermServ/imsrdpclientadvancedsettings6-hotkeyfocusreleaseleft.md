---
title: IMsRdpClientAdvancedSettings6 Хоткэйфокусрелеаселефт, свойство
description: Задает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш Ctrl + Alt + стрелка влево.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Хоткэйфокусрелеаселефт
- Службы удаленных рабочих столов свойства Хоткэйфокусрелеаселефт, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Хоткэйфокусрелеаселефт
- Службы удаленных рабочих столов свойства Хоткэйфокусрелеаселефт, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Хоткэйфокусрелеаселефт
- Службы удаленных рабочих столов свойства Хоткэйфокусрелеаселефт, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Хоткэйфокусрелеаселефт
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801156"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="1ac7c-110">Свойство IMsRdpClientAdvancedSettings6:: Хоткэйфокусрелеаселефт</span><span class="sxs-lookup"><span data-stu-id="1ac7c-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="1ac7c-111">Задает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш Ctrl + Alt + стрелка влево.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="1ac7c-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac7c-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ac7c-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="1ac7c-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1ac7c-114">Property value</span></span>

<span data-ttu-id="1ac7c-115">Новый код виртуального ключа.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac7c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ac7c-116">Remarks</span></span>

<span data-ttu-id="1ac7c-117">Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac7c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1ac7c-118">Requirements</span></span>



| <span data-ttu-id="1ac7c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1ac7c-119">Requirement</span></span> | <span data-ttu-id="1ac7c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1ac7c-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac7c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ac7c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1ac7c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ac7c-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1ac7c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ac7c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1ac7c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ac7c-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1ac7c-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1ac7c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1ac7c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7c-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1ac7c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1ac7c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ac7c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7c-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1ac7c-129">IID</span><span class="sxs-lookup"><span data-stu-id="1ac7c-129">IID</span></span><br/>                      | <span data-ttu-id="1ac7c-130">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="1ac7c-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ac7c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ac7c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac7c-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1ac7c-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1ac7c-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 






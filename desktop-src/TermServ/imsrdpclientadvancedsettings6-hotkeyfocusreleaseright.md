---
title: IMsRdpClientAdvancedSettings6 Хоткэйфокусрелеасеригхт, свойство
description: Указывает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш Ctrl + Alt + стрелка вправо.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Хоткэйфокусрелеасеригхт
- Службы удаленных рабочих столов свойства Хоткэйфокусрелеасеригхт, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Хоткэйфокусрелеасеригхт
- Службы удаленных рабочих столов свойства Хоткэйфокусрелеасеригхт, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Хоткэйфокусрелеасеригхт
- Службы удаленных рабочих столов свойства Хоткэйфокусрелеасеригхт, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Хоткэйфокусрелеасеригхт
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682108"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="ebf0d-110">Свойство IMsRdpClientAdvancedSettings6:: Хоткэйфокусрелеасеригхт</span><span class="sxs-lookup"><span data-stu-id="ebf0d-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="ebf0d-111">Указывает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш Ctrl + Alt + стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="ebf0d-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="ebf0d-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ebf0d-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf0d-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebf0d-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="ebf0d-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ebf0d-114">Property value</span></span>

<span data-ttu-id="ebf0d-115">Новый код виртуального ключа.</span><span class="sxs-lookup"><span data-stu-id="ebf0d-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf0d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ebf0d-116">Remarks</span></span>

<span data-ttu-id="ebf0d-117">Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.</span><span class="sxs-lookup"><span data-stu-id="ebf0d-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf0d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ebf0d-118">Requirements</span></span>



| <span data-ttu-id="ebf0d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ebf0d-119">Requirement</span></span> | <span data-ttu-id="ebf0d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ebf0d-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf0d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebf0d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf0d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebf0d-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ebf0d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebf0d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf0d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebf0d-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ebf0d-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ebf0d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebf0d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf0d-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ebf0d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf0d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebf0d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf0d-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ebf0d-129">IID</span><span class="sxs-lookup"><span data-stu-id="ebf0d-129">IID</span></span><br/>                      | <span data-ttu-id="ebf0d-130">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="ebf0d-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebf0d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebf0d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf0d-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ebf0d-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ebf0d-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ebf0d-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ebf0d-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ebf0d-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 






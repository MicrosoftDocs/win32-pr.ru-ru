---
title: IMsRdpClientAdvancedSettings7 Енаблесуперпан, свойство
description: Указывает или получает логическое значение, указывающее, включен ли параметр Суперпан.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблесуперпан
- Службы удаленных рабочих столов свойства Енаблесуперпан, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Енаблесуперпан
- Службы удаленных рабочих столов свойства Енаблесуперпан, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Енаблесуперпан
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802752"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="73c40-108">Свойство IMsRdpClientAdvancedSettings7:: Енаблесуперпан</span><span class="sxs-lookup"><span data-stu-id="73c40-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="73c40-109">Указывает или получает логическое значение, указывающее, включен ли параметр Суперпан.</span><span class="sxs-lookup"><span data-stu-id="73c40-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="73c40-110">Суперпан — это функция, позволяющая пользователю легко перемещаться по удаленному рабочему столу в полноэкранном режиме, если размеры удаленного рабочего стола больше, чем размеры текущего окна клиента.</span><span class="sxs-lookup"><span data-stu-id="73c40-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="73c40-111">Вместо использования полос прокрутки для навигации по рабочему столу пользователь может указать границу окна, и удаленный рабочий стол будет автоматически прокручиваться в этом направлении.</span><span class="sxs-lookup"><span data-stu-id="73c40-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="73c40-112">Суперпан не поддерживает более одного монитора.</span><span class="sxs-lookup"><span data-stu-id="73c40-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="73c40-113">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="73c40-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c40-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c40-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="73c40-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="73c40-115">Property value</span></span>

<span data-ttu-id="73c40-116">Значение **типа Variant \_ bool** , указывающее, включен ли суперпан.</span><span class="sxs-lookup"><span data-stu-id="73c40-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="73c40-117">Значение **Variant \_ true** указывает, что суперпан включен.</span><span class="sxs-lookup"><span data-stu-id="73c40-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c40-118">Требования</span><span class="sxs-lookup"><span data-stu-id="73c40-118">Requirements</span></span>



| <span data-ttu-id="73c40-119">Требование</span><span class="sxs-lookup"><span data-stu-id="73c40-119">Requirement</span></span> | <span data-ttu-id="73c40-120">Значение</span><span class="sxs-lookup"><span data-stu-id="73c40-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c40-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73c40-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73c40-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73c40-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="73c40-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73c40-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73c40-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73c40-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="73c40-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="73c40-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="73c40-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73c40-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="73c40-127">DLL</span><span class="sxs-lookup"><span data-stu-id="73c40-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73c40-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73c40-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="73c40-129">IID</span><span class="sxs-lookup"><span data-stu-id="73c40-129">IID</span></span><br/>                      | <span data-ttu-id="73c40-130">IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="73c40-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73c40-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73c40-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c40-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="73c40-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="73c40-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="73c40-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 






---
title: IMsRdpClientAdvancedSettings5 Публикмоде, свойство
description: Задает или получает конфигурацию для общедоступного режима. Общедоступный режим не позволяет клиенту кэшировать данные пользователя в локальной системе.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Публикмоде
- Службы удаленных рабочих столов свойства Публикмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Публикмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672574"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="c8991-113">IMsRdpClientAdvancedSettings5: свойство Убликмоде:P</span><span class="sxs-lookup"><span data-stu-id="c8991-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="c8991-114">Задает или получает конфигурацию для общедоступного режима.</span><span class="sxs-lookup"><span data-stu-id="c8991-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="c8991-115">Общедоступный режим не позволяет клиенту кэшировать данные пользователя в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="c8991-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="c8991-116">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c8991-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8991-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8991-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="c8991-118">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c8991-118">Property value</span></span>

<span data-ttu-id="c8991-119">Задает для параметра общего режима значение **Variant \_ true** или **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c8991-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="c8991-120">Если задано **значение \_ true**, параметр общего режима включен.</span><span class="sxs-lookup"><span data-stu-id="c8991-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8991-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c8991-121">Requirements</span></span>



| <span data-ttu-id="c8991-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c8991-122">Requirement</span></span> | <span data-ttu-id="c8991-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c8991-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8991-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8991-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c8991-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8991-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c8991-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8991-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c8991-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8991-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c8991-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c8991-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8991-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8991-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c8991-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c8991-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8991-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8991-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c8991-132">IID</span><span class="sxs-lookup"><span data-stu-id="c8991-132">IID</span></span><br/>                      | <span data-ttu-id="c8991-133">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="c8991-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8991-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8991-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8991-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c8991-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c8991-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c8991-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c8991-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c8991-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c8991-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c8991-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 






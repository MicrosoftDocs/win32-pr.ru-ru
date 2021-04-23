---
title: IMsRdpClientAdvancedSettings5 Коннектионбаршовпинбуттон, свойство
description: Задает или получает конфигурацию кнопки закрепить на панели подключения.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Коннектионбаршовпинбуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовпинбуттон, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Коннектионбаршовпинбуттон
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681834"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="1d4ca-112">Свойство IMsRdpClientAdvancedSettings5:: Коннектионбаршовпинбуттон</span><span class="sxs-lookup"><span data-stu-id="1d4ca-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="1d4ca-113">Задает или получает конфигурацию кнопки закрепить на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="1d4ca-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="1d4ca-114">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1d4ca-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4ca-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d4ca-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="1d4ca-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1d4ca-116">Property value</span></span>

<span data-ttu-id="1d4ca-117">Логическое значение **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="1d4ca-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="1d4ca-118">Значение **true** показывает, что кнопка закрепить на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="1d4ca-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="1d4ca-119">Значение **false** скрывает кнопку закрепить на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="1d4ca-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4ca-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1d4ca-120">Requirements</span></span>



| <span data-ttu-id="1d4ca-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1d4ca-121">Requirement</span></span> | <span data-ttu-id="1d4ca-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1d4ca-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4ca-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d4ca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4ca-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d4ca-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1d4ca-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d4ca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4ca-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d4ca-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1d4ca-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1d4ca-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d4ca-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4ca-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1d4ca-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1d4ca-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4ca-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4ca-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1d4ca-131">IID</span><span class="sxs-lookup"><span data-stu-id="1d4ca-131">IID</span></span><br/>                      | <span data-ttu-id="1d4ca-132">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="1d4ca-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d4ca-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d4ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4ca-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1d4ca-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1d4ca-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1d4ca-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1d4ca-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1d4ca-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1d4ca-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1d4ca-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 






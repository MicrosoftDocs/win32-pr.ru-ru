---
title: Константы TF_LBI_STATUS_ (Ктфутб. h)
description: '\_ \_ Константа TF ЛБИ Status \_ \ указывает состояние элемента языковой панели. Эти значения используются с методом Итфлангбаритемного состояния.'
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803341"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="2e13c-104">\_ \_ \_ \* Константы состояния TF ЛБИ</span><span class="sxs-lookup"><span data-stu-id="2e13c-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="2e13c-105">Константа \*\* \_ tf \_ ЛБИ \_ \* Status\* _ указывает состояние элемента языковой панели.</span><span class="sxs-lookup"><span data-stu-id="2e13c-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="2e13c-106">Эти значения используются с методом [итфлангбаритем:: with Status](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="2e13c-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="2e13c-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="2e13c-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="2e13c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2e13c-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="2e13c-109"><dt>_ \* TF \_ \_ \_ Скрытое состояние ЛБИ \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2e13c-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="2e13c-110">Элемент скрыт.</span><span class="sxs-lookup"><span data-stu-id="2e13c-110">The item is hidden.</span></span> <span data-ttu-id="2e13c-111">Этот стиль игнорируется, если элемент не содержит \_ стиль ХИДДЕНСТАТУСКОНТРОЛ TF ЛБИ \_ Style \_ .</span><span class="sxs-lookup"><span data-stu-id="2e13c-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="2e13c-112"><dt>**Tf \_ \_Состояние ЛБИ \_ disabled**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2e13c-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="2e13c-113">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="2e13c-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="2e13c-114"><dt>**Tf \_ ЛБИ \_ состояние \_ БТН \_ переключено**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="2e13c-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="2e13c-115">Элемент находится в переключенном или нажатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2e13c-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="2e13c-116">Этот стиль игнорируется, если элемент не содержит \_ \_ \_ стиль переключателя TF ЛБИ Style БТН \_ .</span><span class="sxs-lookup"><span data-stu-id="2e13c-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2e13c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2e13c-117">Requirements</span></span>



| <span data-ttu-id="2e13c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2e13c-118">Requirement</span></span> | <span data-ttu-id="2e13c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2e13c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e13c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e13c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e13c-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e13c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2e13c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e13c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e13c-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e13c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e13c-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2e13c-124">Redistributable</span></span><br/>          | <span data-ttu-id="2e13c-125">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="2e13c-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="2e13c-126">Header</span><span class="sxs-lookup"><span data-stu-id="2e13c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e13c-127"><dt>Ктфутб. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e13c-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e13c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="2e13c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e13c-129"><dt>Ктфутб. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e13c-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e13c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e13c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e13c-131">Итфлангбаритем::/Status</span><span class="sxs-lookup"><span data-stu-id="2e13c-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 






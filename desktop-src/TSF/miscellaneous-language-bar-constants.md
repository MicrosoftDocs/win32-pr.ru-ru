---
title: Различные константы языковой панели (Ктфутб. h)
description: Различные константы языковой панели задают определенные свойства языковых панелей.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415985"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="adf34-103">Различные константы языковой панели</span><span class="sxs-lookup"><span data-stu-id="adf34-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="adf34-104">Различные константы языковой панели задают определенные свойства языковых панелей.</span><span class="sxs-lookup"><span data-stu-id="adf34-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="adf34-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="adf34-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="adf34-106">Описание</span><span class="sxs-lookup"><span data-stu-id="adf34-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="adf34-107"><dt>**Tf \_ ДТЛБИ \_ усепрофилеикон**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="adf34-108">Элемент языковой панели системы должен отображать значок, указанный для профиля языка.</span><span class="sxs-lookup"><span data-stu-id="adf34-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="adf34-109">Используется в методах [итфсистемдевицетипелангбаритем:: жетиконмоде](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) и [Итфсистемдевицетипелангбаритем:: сетиконмоде](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .</span><span class="sxs-lookup"><span data-stu-id="adf34-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="adf34-110"><dt>**Tf \_ ИНВАЛИДМЕНУИТЕМ**</dt> <dt>(UINT) (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="adf34-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="adf34-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="adf34-112"><dt>**Tf \_ ЛБИ \_ бмпф \_ по вертикали**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="adf34-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="adf34-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="adf34-114"><dt>**Tf \_ ЛБИ \_ DESC \_ maxlen**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="adf34-115">Длина в WCHAR символах для члена структуры [tf \_ Лангбаритеминфо. сздескриптион](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span><span class="sxs-lookup"><span data-stu-id="adf34-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="adf34-116">Требования</span><span class="sxs-lookup"><span data-stu-id="adf34-116">Requirements</span></span>



| <span data-ttu-id="adf34-117">Требование</span><span class="sxs-lookup"><span data-stu-id="adf34-117">Requirement</span></span> | <span data-ttu-id="adf34-118">Значение</span><span class="sxs-lookup"><span data-stu-id="adf34-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adf34-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adf34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="adf34-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="adf34-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="adf34-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adf34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="adf34-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="adf34-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="adf34-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="adf34-123">Redistributable</span></span><br/>          | <span data-ttu-id="adf34-124">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="adf34-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="adf34-125">Header</span><span class="sxs-lookup"><span data-stu-id="adf34-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf34-126"><dt>Ктфутб. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="adf34-127">IDL</span><span class="sxs-lookup"><span data-stu-id="adf34-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="adf34-128"><dt>Ктфутб. idl</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf34-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adf34-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf34-130">Итфсистемдевицетипелангбаритем:: Жетиконмоде</span><span class="sxs-lookup"><span data-stu-id="adf34-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="adf34-131">Итфсистемдевицетипелангбаритем:: Сетиконмоде</span><span class="sxs-lookup"><span data-stu-id="adf34-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="adf34-132">TF \_ лангбаритеминфо</span><span class="sxs-lookup"><span data-stu-id="adf34-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 






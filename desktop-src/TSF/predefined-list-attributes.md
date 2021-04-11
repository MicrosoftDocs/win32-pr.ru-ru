---
title: Стандартные атрибуты списка (Тсаттрид. h)
description: Следующие значения обозначают атрибуты списка, полученные с помощью метода ITfContext Жетапппроперти. В него включаются формат данных и содержимое каждого типа свойства.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Предварительно определенные атрибуты списка. Платформа текстовых служб
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137035"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="434e6-105">Стандартные атрибуты списка</span><span class="sxs-lookup"><span data-stu-id="434e6-105">Predefined List Attributes</span></span>

<span data-ttu-id="434e6-106">Следующие значения обозначают атрибуты списка, полученные с помощью метода [ITfContext:: жетапппроперти](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="434e6-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="434e6-107">В него включаются формат данных и содержимое каждого типа свойства.</span><span class="sxs-lookup"><span data-stu-id="434e6-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="434e6-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="434e6-108">Properties</span></span>



| <span data-ttu-id="434e6-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="434e6-109">Property</span></span>                          | <span data-ttu-id="434e6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="434e6-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="434e6-111">\_Список тсаттрид</span><span class="sxs-lookup"><span data-stu-id="434e6-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="434e6-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="434e6-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="434e6-113">\_Левелиндел списка \_ тсаттрид</span><span class="sxs-lookup"><span data-stu-id="434e6-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="434e6-114">Содержит уровень индекса списка.</span><span class="sxs-lookup"><span data-stu-id="434e6-114">Contains the index level of the list.</span></span> <span data-ttu-id="434e6-115">1 — это внешний уровень, 2 — следующий уровень и т. д.</span><span class="sxs-lookup"><span data-stu-id="434e6-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="434e6-116">\_Тип списка \_ тсаттрид</span><span class="sxs-lookup"><span data-stu-id="434e6-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="434e6-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="434e6-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="434e6-118">\_Тип списка \_ тсаттрид \_ Арабский</span><span class="sxs-lookup"><span data-stu-id="434e6-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="434e6-119">Содержит ненулевое значение, если список является арабским числом или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="434e6-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="434e6-120">\_ \_ Маркер типа списка \_ тсаттрид</span><span class="sxs-lookup"><span data-stu-id="434e6-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="434e6-121">Содержит ненулевое значение, если список является маркированным списком, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="434e6-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="434e6-122">ТСАТТРИД \_ \_ тип списка \_ ловерлеттер</span><span class="sxs-lookup"><span data-stu-id="434e6-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="434e6-123">Содержит ненулевое значение, если список является списком с прописными буквами или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="434e6-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="434e6-124">ТСАТТРИД \_ \_ тип списка \_ ловерроман</span><span class="sxs-lookup"><span data-stu-id="434e6-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="434e6-125">Содержит ненулевое значение, если список имеет римские цифры в нижнем регистре или в противном случае ноль.</span><span class="sxs-lookup"><span data-stu-id="434e6-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="434e6-126">ТСАТТРИД \_ \_ тип списка \_ упперлеттер</span><span class="sxs-lookup"><span data-stu-id="434e6-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="434e6-127">Содержит ненулевое значение, если список является списком с прописными буквами или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="434e6-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="434e6-128">ТСАТТРИД \_ \_ тип списка \_ упперроман</span><span class="sxs-lookup"><span data-stu-id="434e6-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="434e6-129">Содержит ненулевое значение, если список является списком цифр в верхнем регистре или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="434e6-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="434e6-130">Требования</span><span class="sxs-lookup"><span data-stu-id="434e6-130">Requirements</span></span>



| <span data-ttu-id="434e6-131">Требование</span><span class="sxs-lookup"><span data-stu-id="434e6-131">Requirement</span></span> | <span data-ttu-id="434e6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="434e6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="434e6-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="434e6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="434e6-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="434e6-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="434e6-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="434e6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="434e6-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="434e6-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="434e6-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="434e6-137">Redistributable</span></span><br/>          | <span data-ttu-id="434e6-138">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="434e6-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="434e6-139">Header</span><span class="sxs-lookup"><span data-stu-id="434e6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="434e6-140"><dt>Тсаттрид. h</dt></span><span class="sxs-lookup"><span data-stu-id="434e6-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434e6-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="434e6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434e6-142">ITfContext:: Жетапппроперти</span><span class="sxs-lookup"><span data-stu-id="434e6-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 


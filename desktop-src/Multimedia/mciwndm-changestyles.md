---
title: Сообщение MCIWNDM_CHANGESTYLES (VFW. h)
description: Сообщение МЦИВНДМ \_ чанжестилес изменяет стили, используемые в окне мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндчанжестилес.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650366"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="c36c4-105">\_Сообщение мЦивндм чанжестилес</span><span class="sxs-lookup"><span data-stu-id="c36c4-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="c36c4-106">Сообщение **мЦивндм \_ чанжестилес** изменяет стили, используемые в окне мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="c36c4-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="c36c4-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .</span><span class="sxs-lookup"><span data-stu-id="c36c4-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="c36c4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c36c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36c4-109"><span id="mask"></span><span id="MASK"></span>*виде*</span><span class="sxs-lookup"><span data-stu-id="c36c4-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="c36c4-110">Маска, определяющая стили, которые могут изменяться.</span><span class="sxs-lookup"><span data-stu-id="c36c4-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="c36c4-111">Эта маска является побитовым оператором или для всех стилей, которые разрешено изменять.</span><span class="sxs-lookup"><span data-stu-id="c36c4-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="c36c4-112"><span id="value"></span><span id="VALUE"></span>*значений*</span><span class="sxs-lookup"><span data-stu-id="c36c4-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="c36c4-113">Новые параметры стиля для окна.</span><span class="sxs-lookup"><span data-stu-id="c36c4-113">New style settings for the window.</span></span> <span data-ttu-id="c36c4-114">Укажите ноль для этого параметра, чтобы отключить все стили, определенные в маске.</span><span class="sxs-lookup"><span data-stu-id="c36c4-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="c36c4-115">Список доступных стилей см. в разделе Функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="c36c4-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c36c4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c36c4-116">Return Value</span></span>

<span data-ttu-id="c36c4-117">Возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c36c4-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36c4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c36c4-118">Requirements</span></span>



| <span data-ttu-id="c36c4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c36c4-119">Requirement</span></span> | <span data-ttu-id="c36c4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c36c4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c36c4-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c36c4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c36c4-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c36c4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c36c4-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c36c4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c36c4-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c36c4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c36c4-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c36c4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c36c4-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c36c4-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c36c4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c36c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c36c4-128">**мЦивндкреате**</span><span class="sxs-lookup"><span data-stu-id="c36c4-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="c36c4-129">**мЦивндчанжестилес**</span><span class="sxs-lookup"><span data-stu-id="c36c4-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 






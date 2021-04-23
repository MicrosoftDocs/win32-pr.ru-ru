---
title: Сообщение EM_GETCUEBANNER (Коммктрл. h)
description: Возвращает текст, который отображается как текстовая подсказка или Совет в элементе управления "поле ввода".
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Элементы управления Windows для EM_GETCUEBANNER сообщений
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989334"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="dceeb-104">\_Сообщение ЖЕТКУЕБАННЕР EM</span><span class="sxs-lookup"><span data-stu-id="dceeb-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="dceeb-105">Возвращает текст, который отображается как текстовая подсказка или Совет в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="dceeb-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dceeb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dceeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dceeb-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dceeb-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dceeb-108">Указатель на буфер Юникода, который получает текстовый набор в качестве текстовой подсказки.</span><span class="sxs-lookup"><span data-stu-id="dceeb-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="dceeb-109">Вызывающий объект отвечает за выделение буфера.</span><span class="sxs-lookup"><span data-stu-id="dceeb-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dceeb-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dceeb-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dceeb-111">Размер буфера, на который указывает *wParam* в **вчарс**, включая завершающее **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dceeb-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dceeb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dceeb-112">Return value</span></span>

<span data-ttu-id="dceeb-113">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dceeb-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dceeb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dceeb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dceeb-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="dceeb-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="dceeb-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dceeb-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dceeb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="dceeb-117">Requirements</span></span>



| <span data-ttu-id="dceeb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="dceeb-118">Requirement</span></span> | <span data-ttu-id="dceeb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dceeb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dceeb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dceeb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dceeb-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dceeb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dceeb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dceeb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dceeb-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dceeb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dceeb-124">Header</span><span class="sxs-lookup"><span data-stu-id="dceeb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dceeb-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dceeb-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dceeb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dceeb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dceeb-127">**Изменить \_ жеткуебаннертекст**</span><span class="sxs-lookup"><span data-stu-id="dceeb-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 






---
title: Сообщение TB_SETDRAWTEXTFLAGS (Коммктрл. h)
description: Задает флаги рисования текста для панели инструментов.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Элементы управления Windows для TB_SETDRAWTEXTFLAGS сообщений
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989064"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="5f938-104">\_Сообщение СЕТДРАВТЕКСТФЛАГС ТБ</span><span class="sxs-lookup"><span data-stu-id="5f938-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="5f938-105">Задает флаги рисования текста для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="5f938-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f938-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f938-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f938-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f938-108">Один или несколько \_ флагов DT, указанных в [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), которые указывают, какие биты в *lParam* будут использоваться при рисовании текста.</span><span class="sxs-lookup"><span data-stu-id="5f938-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="5f938-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f938-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f938-110">Один или несколько \_ флагов DT, заданных в [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), которые указывают, как будет нарисован текст кнопки.</span><span class="sxs-lookup"><span data-stu-id="5f938-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="5f938-111">Это значение будет передано функции **DrawText** при прорисовке текста кнопки.</span><span class="sxs-lookup"><span data-stu-id="5f938-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f938-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f938-112">Return value</span></span>

<span data-ttu-id="5f938-113">Возвращает предыдущие флаги рисования текста.</span><span class="sxs-lookup"><span data-stu-id="5f938-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f938-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f938-114">Remarks</span></span>

<span data-ttu-id="5f938-115">Параметр *wParam* позволяет указать, какие флаги будут использоваться при рисовании текста, даже если эти флаги отключены.</span><span class="sxs-lookup"><span data-stu-id="5f938-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="5f938-116">Например, если не нужно, \_ чтобы флаг центра DT использовался при рисовании текста, необходимо добавить в \_ *wParam* флаг «центр DT» и не указывать в параметре \_ *lParam* флаг «центр DT».</span><span class="sxs-lookup"><span data-stu-id="5f938-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="5f938-117">Это предотвращает передачу элементом управления \_ флага центра DT в функцию [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="5f938-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f938-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5f938-118">Requirements</span></span>



| <span data-ttu-id="5f938-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5f938-119">Requirement</span></span> | <span data-ttu-id="5f938-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5f938-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f938-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f938-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f938-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f938-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f938-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f938-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f938-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f938-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f938-125">Header</span><span class="sxs-lookup"><span data-stu-id="5f938-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f938-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f938-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


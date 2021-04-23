---
title: Сообщение CB_GETCUEBANNER (Winuser. h)
description: Возвращает текст баннера подсказки, отображаемый в элементе управления "поле ввода" поля со списком. Отправляйте это сообщение явным образом или с помощью \_ макроса Жеткуебаннертекст ComboBox.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- Элементы управления Windows для CB_GETCUEBANNER сообщений
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892174"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="648f8-105">\_Сообщение ЖЕТКУЕБАННЕР CB</span><span class="sxs-lookup"><span data-stu-id="648f8-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="648f8-106">Возвращает текст баннера подсказки, отображаемый в элементе управления "поле ввода" поля со списком.</span><span class="sxs-lookup"><span data-stu-id="648f8-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="648f8-107">Отправляйте это сообщение явным образом или с помощью макроса [**\_ жеткуебаннертекст ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .</span><span class="sxs-lookup"><span data-stu-id="648f8-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="648f8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="648f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="648f8-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="648f8-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="648f8-110">Указатель на буфер строки в Юникоде, который получает текст объявления подсказки.</span><span class="sxs-lookup"><span data-stu-id="648f8-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="648f8-111">Вызывающее приложение отвечает за выделение памяти для буфера.</span><span class="sxs-lookup"><span data-stu-id="648f8-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="648f8-112">Размер буфера должен быть равен длине строки заголовка подсказки в **вчарс**, плюс 1 для завершающего **нулевого значения** **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="648f8-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="648f8-113">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="648f8-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="648f8-114">Размер буфера, на который указывает *лпквтекст* в **вчарс**.</span><span class="sxs-lookup"><span data-stu-id="648f8-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="648f8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="648f8-115">Return value</span></span>

<span data-ttu-id="648f8-116">Возвращает 1 в случае успеха или значение ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="648f8-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="648f8-117">Если текст объявления подсказки отсутствует, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="648f8-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="648f8-118">Если вызывающему приложению не удается выделить буфер или задать параметр *lParam* перед отправкой этого сообщения, может возникнуть неопределенное поведение, и возвращаемое значение может быть ненадежным.</span><span class="sxs-lookup"><span data-stu-id="648f8-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="648f8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="648f8-119">Requirements</span></span>



| <span data-ttu-id="648f8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="648f8-120">Requirement</span></span> | <span data-ttu-id="648f8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="648f8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="648f8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="648f8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="648f8-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="648f8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="648f8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="648f8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="648f8-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="648f8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="648f8-126">Header</span><span class="sxs-lookup"><span data-stu-id="648f8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="648f8-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="648f8-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="648f8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="648f8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648f8-129">Возможности поля со списком</span><span class="sxs-lookup"><span data-stu-id="648f8-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 






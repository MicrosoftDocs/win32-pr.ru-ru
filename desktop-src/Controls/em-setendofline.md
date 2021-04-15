---
title: Сообщение EM_SETENDOFLINE (Коммктрл. h)
description: Задает символ конца строки, используемый при вставке LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Элементы управления Windows для EM_SETENDOFLINE сообщений
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492462"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="b8cd6-104">\_Сообщение СЕТЕНДОФЛИНЕ EM</span><span class="sxs-lookup"><span data-stu-id="b8cd6-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="b8cd6-105">Задает символ конца строки, используемый при вставке LineBreak.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8cd6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8cd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8cd6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8cd6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8cd6-108">Задает символ конца строки, используемый при вставке LineBreak.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="b8cd6-109">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-109">This can be one of the following values.</span></span>


| <span data-ttu-id="b8cd6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cd6-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="b8cd6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cd6-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="b8cd6-112"><dt>**EC \_ ендофлине \_ детектфромконтент**</dt></span><span class="sxs-lookup"><span data-stu-id="b8cd6-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="b8cd6-113">Задает символ конца строки, используемый для New линебреакс для символа, используемого текущим документом.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="b8cd6-114"><dt>**EC \_ ендофлине \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="b8cd6-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="b8cd6-115">Задает символ конца строки, используемый для новой линебреакс для возврата каретки, за которым следует перевод строки (CRLF).</span><span class="sxs-lookup"><span data-stu-id="b8cd6-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="b8cd6-116"><dt>**EC \_ ендофлине \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="b8cd6-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="b8cd6-117">Задает символ конца строки, используемый для нового линебреакс для возврата каретки (CR).</span><span class="sxs-lookup"><span data-stu-id="b8cd6-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="b8cd6-118"><dt>**EC \_ ендофлине \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="b8cd6-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="b8cd6-119">Задает символ конца строки, используемый для новой линебреакс для перевода строки (LF).</span><span class="sxs-lookup"><span data-stu-id="b8cd6-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="b8cd6-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8cd6-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8cd6-121">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8cd6-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8cd6-122">Return value</span></span>

<span data-ttu-id="b8cd6-123">Если операция выполнена удачно, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="b8cd6-124">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b8cd6-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cd6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8cd6-125">Remarks</span></span>

<span data-ttu-id="b8cd6-126">Если кодировка конца строки равна **EC \_ ендофлине \_ детектфромконтент**, элемент управления "поле ввода" будет обнаруживать только символы конца строки, поддерживаемые в соответствии с его расширенным стилем окна. см. раздел [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="b8cd6-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cd6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b8cd6-127">Requirements</span></span>



| <span data-ttu-id="b8cd6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b8cd6-128">Requirement</span></span> | <span data-ttu-id="b8cd6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cd6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cd6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8cd6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cd6-131">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="b8cd6-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8cd6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8cd6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cd6-133">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="b8cd6-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8cd6-134">Header</span><span class="sxs-lookup"><span data-stu-id="b8cd6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8cd6-135"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8cd6-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8cd6-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8cd6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cd6-137">\**EM \_ жетендофлине*</span><span class="sxs-lookup"><span data-stu-id="b8cd6-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 






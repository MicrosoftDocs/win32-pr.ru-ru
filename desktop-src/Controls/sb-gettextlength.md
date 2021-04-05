---
title: Сообщение SB_GETTEXTLENGTH (Коммктрл. h)
description: Извлекает длину текста в символах из указанной части окна состояния.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Элементы управления Windows для SB_GETTEXTLENGTH сообщений
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989075"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="cba8b-104">\_Сообщение SB жеттекстленгс</span><span class="sxs-lookup"><span data-stu-id="cba8b-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="cba8b-105">Извлекает длину текста в символах из указанной части окна состояния.</span><span class="sxs-lookup"><span data-stu-id="cba8b-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="cba8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cba8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba8b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cba8b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cba8b-108">Отсчитываемый от нуля индекс части, из которой требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="cba8b-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="cba8b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cba8b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cba8b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cba8b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba8b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cba8b-111">Return value</span></span>

<span data-ttu-id="cba8b-112">Возвращает 32-разрядное значение, состоящее из 2 16-разрядных значений.</span><span class="sxs-lookup"><span data-stu-id="cba8b-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="cba8b-113">Нижнее слово указывает длину текста в символах.</span><span class="sxs-lookup"><span data-stu-id="cba8b-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="cba8b-114">В верхнем слове указывается тип операции, используемой для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="cba8b-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="cba8b-115">Тип может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="cba8b-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="cba8b-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cba8b-116">Return code</span></span>                                                                                    | <span data-ttu-id="cba8b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cba8b-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cba8b-118"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8b-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="cba8b-119">Текст отображается с границей, которая отображается ниже плоскости окна.</span><span class="sxs-lookup"><span data-stu-id="cba8b-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="cba8b-120"><dt>**SBT \_ НЕграницы**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8b-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="cba8b-121">Текст отображается без границ.</span><span class="sxs-lookup"><span data-stu-id="cba8b-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="cba8b-122"><dt>**SBT \_ овнердрав**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8b-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="cba8b-123">Текст рисуется родительским окном.</span><span class="sxs-lookup"><span data-stu-id="cba8b-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="cba8b-124"><dt>**SBT \_ POPOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8b-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="cba8b-125">Текст отображается с границей, которая отображается выше плоскости окна.</span><span class="sxs-lookup"><span data-stu-id="cba8b-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="cba8b-126"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="cba8b-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="cba8b-127">Текст будет отображаться в обратном направлении к тексту в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="cba8b-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cba8b-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cba8b-128">Remarks</span></span>

<span data-ttu-id="cba8b-129">Нормальный отображаемый текст Windows слева направо (LTR).</span><span class="sxs-lookup"><span data-stu-id="cba8b-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="cba8b-130">Windows может быть *зеркальным* отображением таких языков, как иврит или арабский, которые читаются справа налево.</span><span class="sxs-lookup"><span data-stu-id="cba8b-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="cba8b-131">Если \_ задано значение SBT RTLREADING, то указанный текст окна состояния будет читаться в обратном направлении от текста в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="cba8b-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="cba8b-132">Это сообщение возвращает максимальную длину строки в 65 535 символов.</span><span class="sxs-lookup"><span data-stu-id="cba8b-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="cba8b-133">Если фактическая длина текстовой строки превышает это значение, сообщение [**SB \_ gettext**](sb-gettext.md) усекает его.</span><span class="sxs-lookup"><span data-stu-id="cba8b-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba8b-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cba8b-134">Requirements</span></span>



| <span data-ttu-id="cba8b-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cba8b-135">Requirement</span></span> | <span data-ttu-id="cba8b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cba8b-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cba8b-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cba8b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cba8b-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cba8b-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cba8b-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cba8b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cba8b-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cba8b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cba8b-141">Header</span><span class="sxs-lookup"><span data-stu-id="cba8b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba8b-142"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba8b-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cba8b-143">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="cba8b-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cba8b-144">**SB \_ ЖЕТТЕКСТЛЕНГСВ** (Юникод) и **SB \_ жеттекстленгса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cba8b-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 






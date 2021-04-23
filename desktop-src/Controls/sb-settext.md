---
title: Сообщение SB_SETTEXT (Коммктрл. h)
description: Задает текст в указанной части окна состояния.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Элементы управления Windows для SB_SETTEXT сообщений
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136823"
---
# <a name="sb_settext-message"></a><span data-ttu-id="261f1-104">\_Сообщение SB SETTEXT</span><span class="sxs-lookup"><span data-stu-id="261f1-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="261f1-105">Задает текст в указанной части окна состояния.</span><span class="sxs-lookup"><span data-stu-id="261f1-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="261f1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="261f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="261f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="261f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="261f1-108">[**Лобите**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) слово низкого порядка Указывает отсчитываемый от нуля индекс части, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="261f1-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="261f1-109">Если **лобите** имеет значение SB \_ симплеид, то окно состояния считается строкой состояния простого режима, то есть строкой состояния только с одной частью.</span><span class="sxs-lookup"><span data-stu-id="261f1-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="261f1-110">[**Хибите**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) слово низкого порядка указывает тип операции рисования.</span><span class="sxs-lookup"><span data-stu-id="261f1-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="261f1-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="261f1-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="261f1-112">Слово « *wParam* » высокого порядка не учитывается.</span><span class="sxs-lookup"><span data-stu-id="261f1-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="261f1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="261f1-113">Value</span></span></th>
<th><span data-ttu-id="261f1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="261f1-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="261f1-115"><dt><strong>0,0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="261f1-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="261f1-116">Текст отображается с границей, которая отображается ниже плоскости окна.</span><span class="sxs-lookup"><span data-stu-id="261f1-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="261f1-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="261f1-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="261f1-118">Текст отображается без границ.</span><span class="sxs-lookup"><span data-stu-id="261f1-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="261f1-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="261f1-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="261f1-120">Текст рисуется родительским окном.</span><span class="sxs-lookup"><span data-stu-id="261f1-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="261f1-121">Строка состояния простого режима не поддерживает рисование владельцем.</span><span class="sxs-lookup"><span data-stu-id="261f1-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="261f1-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="261f1-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="261f1-123">Текст отображается с границей, которая отображается выше плоскости окна.</span><span class="sxs-lookup"><span data-stu-id="261f1-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="261f1-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="261f1-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="261f1-125">Текст будет отображаться в обратном направлении к тексту в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="261f1-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="261f1-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="261f1-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="261f1-127">Символы табуляции игнорируются.</span><span class="sxs-lookup"><span data-stu-id="261f1-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="261f1-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="261f1-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="261f1-129">Указатель на строку, завершающуюся нулем, которая указывает текст для установки.</span><span class="sxs-lookup"><span data-stu-id="261f1-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="261f1-130">Если аргумент *wParam* имеет значение SBT \_ овнердрав, этот параметр представляет 32 бит данных.</span><span class="sxs-lookup"><span data-stu-id="261f1-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="261f1-131">Родительское окно должно интерпретировать данные и нарисовать текст при получении сообщения [**WM \_ DRAWITEM**](wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="261f1-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="261f1-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="261f1-132">Return value</span></span>

<span data-ttu-id="261f1-133">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="261f1-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="261f1-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="261f1-134">Remarks</span></span>

<span data-ttu-id="261f1-135">Сообщение сделает недействительным измененную часть окна, что привело бы к отображению нового текста, когда окно затем получит сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="261f1-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="261f1-136">Нормальный отображаемый текст Windows слева направо (LTR).</span><span class="sxs-lookup"><span data-stu-id="261f1-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="261f1-137">Windows может быть *зеркальным* отображением таких языков, как иврит или арабский, которые читаются справа налево.</span><span class="sxs-lookup"><span data-stu-id="261f1-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="261f1-138">Если задан параметр SBT \_ RTLREADING, строка *lParam* будет считаться в обратном направлении от текста в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="261f1-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="261f1-139">Требования</span><span class="sxs-lookup"><span data-stu-id="261f1-139">Requirements</span></span>



| <span data-ttu-id="261f1-140">Требование</span><span class="sxs-lookup"><span data-stu-id="261f1-140">Requirement</span></span> | <span data-ttu-id="261f1-141">Значение</span><span class="sxs-lookup"><span data-stu-id="261f1-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="261f1-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="261f1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="261f1-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="261f1-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="261f1-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="261f1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="261f1-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="261f1-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="261f1-146">Header</span><span class="sxs-lookup"><span data-stu-id="261f1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="261f1-147"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="261f1-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="261f1-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="261f1-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="261f1-149">**SB \_ СЕТТЕКСТВ** (Юникод) и **SB \_ сеттекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="261f1-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="261f1-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="261f1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261f1-151">**SB ( \_ SMS)**</span><span class="sxs-lookup"><span data-stu-id="261f1-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 


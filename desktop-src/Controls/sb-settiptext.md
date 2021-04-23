---
title: Сообщение SB_SETTIPTEXT (Коммктрл. h)
description: Задает текст подсказки для части в строке состояния. Чтобы включить подсказки, строка состояния должна быть создана с помощью \_ стиля подсказок SBT.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Элементы управления Windows для SB_SETTIPTEXT сообщений
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491988"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="4851f-105">\_Сообщение SB сеттиптекст</span><span class="sxs-lookup"><span data-stu-id="4851f-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="4851f-106">Задает текст подсказки для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="4851f-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="4851f-107">Чтобы включить подсказки, строка состояния должна быть создана с помощью стиля [**\_ подсказок SBT**](status-bar-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4851f-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="4851f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4851f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4851f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4851f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4851f-110">Отсчитываемый от нуля индекс части, которая будет принимать текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="4851f-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="4851f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4851f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4851f-112">Указатель на символьный буфер, содержащий новый текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="4851f-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4851f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4851f-113">Return value</span></span>

<span data-ttu-id="4851f-114">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4851f-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4851f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4851f-115">Remarks</span></span>

<span data-ttu-id="4851f-116">Этот текст подсказки отображается в двух ситуациях:</span><span class="sxs-lookup"><span data-stu-id="4851f-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="4851f-117">Если соответствующая панель в строке состояния содержит только значок.</span><span class="sxs-lookup"><span data-stu-id="4851f-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="4851f-118">Когда соответствующая панель в строке состояния содержит текст, усеченный из-за размера панели.</span><span class="sxs-lookup"><span data-stu-id="4851f-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="4851f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4851f-119">Requirements</span></span>



| <span data-ttu-id="4851f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4851f-120">Requirement</span></span> | <span data-ttu-id="4851f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4851f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4851f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4851f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4851f-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4851f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4851f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4851f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4851f-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4851f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4851f-126">Header</span><span class="sxs-lookup"><span data-stu-id="4851f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4851f-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4851f-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4851f-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4851f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4851f-129">**SB \_ СЕТТИПТЕКСТВ** (Юникод) и **SB \_ сеттиптекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4851f-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 






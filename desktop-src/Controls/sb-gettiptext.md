---
title: Сообщение SB_GETTIPTEXT (Коммктрл. h)
description: Извлекает текст подсказки для части в строке состояния. Чтобы включить подсказки, необходимо создать строку состояния с помощью \_ стиля подсказок SBT.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Элементы управления Windows для SB_GETTIPTEXT сообщений
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892353"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="15467-105">\_Сообщение SB жеттиптекст</span><span class="sxs-lookup"><span data-stu-id="15467-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="15467-106">Извлекает текст подсказки для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="15467-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="15467-107">Чтобы включить подсказки, необходимо создать строку состояния с помощью стиля [**\_ подсказок SBT**](status-bar-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="15467-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="15467-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15467-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15467-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15467-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15467-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает отсчитываемый от нуля индекс части, которая получает текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="15467-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="15467-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает размер буфера в параметре *lParam* в символах.</span><span class="sxs-lookup"><span data-stu-id="15467-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="15467-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15467-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15467-113">Указатель на символьный буфер, который получает текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="15467-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15467-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15467-114">Return value</span></span>

<span data-ttu-id="15467-115">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="15467-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="15467-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15467-116">Remarks</span></span>

<span data-ttu-id="15467-117">**Предупреждение системы безопасности:** Неправильное использование этого сообщения может привести к проблемам с приложением.</span><span class="sxs-lookup"><span data-stu-id="15467-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="15467-118">Например, если текст слишком велик для буфера *lParam* , это может привести к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="15467-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="15467-119">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="15467-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="15467-120">Требования</span><span class="sxs-lookup"><span data-stu-id="15467-120">Requirements</span></span>



| <span data-ttu-id="15467-121">Требование</span><span class="sxs-lookup"><span data-stu-id="15467-121">Requirement</span></span> | <span data-ttu-id="15467-122">Значение</span><span class="sxs-lookup"><span data-stu-id="15467-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15467-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15467-123">Minimum supported client</span></span><br/> | <span data-ttu-id="15467-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15467-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15467-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15467-125">Minimum supported server</span></span><br/> | <span data-ttu-id="15467-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="15467-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15467-127">Header</span><span class="sxs-lookup"><span data-stu-id="15467-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="15467-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="15467-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="15467-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="15467-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="15467-130">**SB \_ ЖЕТТИПТЕКСТВ** (Юникод) и **SB \_ жеттиптекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="15467-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 


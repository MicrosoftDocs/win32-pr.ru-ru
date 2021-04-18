---
title: Сообщение TTM_ENUMTOOLS (Коммктрл. h)
description: Извлекает сведения, которые хранит элемент управления ToolTip о текущем инструменте \ 8212; это средство, для которого в настоящий момент отображается текст всплывающей подсказки.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Элементы управления Windows для TTM_ENUMTOOLS сообщений
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490683"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="0fa23-104">\_Сообщение ТТМ енумтулс</span><span class="sxs-lookup"><span data-stu-id="0fa23-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="0fa23-105">Извлекает сведения, которые хранит элемент управления ToolTip о текущем инструменте, то есть инструмент, для которого подсказка в данный момент отображает текст.</span><span class="sxs-lookup"><span data-stu-id="0fa23-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fa23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fa23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fa23-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fa23-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa23-108">Отсчитываемый от нуля индекс инструмента, для которого требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="0fa23-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="0fa23-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fa23-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa23-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , которая получает сведения о средстве.</span><span class="sxs-lookup"><span data-stu-id="0fa23-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="0fa23-111">Перед отправкой этого сообщения установите для элемента **кбсизе** этой структуры значение sizeof (тулинфо).</span><span class="sxs-lookup"><span data-stu-id="0fa23-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="0fa23-112">Выделение буфера.</span><span class="sxs-lookup"><span data-stu-id="0fa23-112">Allocate a buffer.</span></span> <span data-ttu-id="0fa23-113">Установите элемент **лпсзтекст** , чтобы он указывал на буфер для получения текста инструмента.</span><span class="sxs-lookup"><span data-stu-id="0fa23-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="0fa23-114">Невозможно определить требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="0fa23-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="0fa23-115">Тем не менее, текст инструмента, возвращаемый в **лпсзтекст** член структуры **тулинфо** , имеет максимальную длину 80 **Тчарс**, включая завершающее **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0fa23-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="0fa23-116">Если текст превышает эту длину, он усекается.</span><span class="sxs-lookup"><span data-stu-id="0fa23-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fa23-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fa23-117">Return value</span></span>

<span data-ttu-id="0fa23-118">Возвращает **значение true** , если какие бы то ни было средства были перечислены, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0fa23-118">Returns **TRUE** if any tools are enumerated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fa23-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fa23-119">Remarks</span></span>

<span data-ttu-id="0fa23-120">**Предупреждение системы безопасности:** Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="0fa23-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="0fa23-121">Это сообщение не дает получателю сообщения способ определить размер буфера или указать размер буфера в буфере.</span><span class="sxs-lookup"><span data-stu-id="0fa23-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="0fa23-122">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa23-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa23-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0fa23-123">Requirements</span></span>



| <span data-ttu-id="0fa23-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0fa23-124">Requirement</span></span> | <span data-ttu-id="0fa23-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0fa23-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa23-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fa23-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa23-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fa23-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fa23-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fa23-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa23-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0fa23-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fa23-130">Header</span><span class="sxs-lookup"><span data-stu-id="0fa23-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fa23-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fa23-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0fa23-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="0fa23-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0fa23-133">**ТТМ \_ ЕНУМТУЛСВ** (Юникод) и **ТТМ \_ енумтулса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0fa23-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 






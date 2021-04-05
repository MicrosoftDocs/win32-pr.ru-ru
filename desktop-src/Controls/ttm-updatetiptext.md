---
title: Сообщение TTM_UPDATETIPTEXT (Коммктрл. h)
description: Задает текст подсказки для инструмента.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Элементы управления Windows для TTM_UPDATETIPTEXT сообщений
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136402"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="5c8ab-104">\_Сообщение ТТМ упдатетиптекст</span><span class="sxs-lookup"><span data-stu-id="5c8ab-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="5c8ab-105">Задает текст подсказки для инструмента.</span><span class="sxs-lookup"><span data-stu-id="5c8ab-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c8ab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c8ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c8ab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c8ab-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5c8ab-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5c8ab-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5c8ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c8ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c8ab-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5c8ab-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="5c8ab-111">Члены **хинст** и **лпсзтекст** должны задавать обработчик экземпляра и адрес текста.</span><span class="sxs-lookup"><span data-stu-id="5c8ab-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="5c8ab-112">Элементы **HWND** и **uId** указывают средство для обновления.</span><span class="sxs-lookup"><span data-stu-id="5c8ab-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="5c8ab-113">Перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="5c8ab-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c8ab-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c8ab-114">Return value</span></span>

<span data-ttu-id="5c8ab-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="5c8ab-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8ab-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5c8ab-116">Requirements</span></span>



| <span data-ttu-id="5c8ab-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5c8ab-117">Requirement</span></span> | <span data-ttu-id="5c8ab-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5c8ab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8ab-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c8ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c8ab-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c8ab-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c8ab-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c8ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c8ab-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c8ab-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c8ab-123">Header</span><span class="sxs-lookup"><span data-stu-id="5c8ab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c8ab-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c8ab-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5c8ab-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5c8ab-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5c8ab-126">**ТТМ \_ УПДАТЕТИПТЕКСТВ** (Юникод) и **ТТМ \_ упдатетиптекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5c8ab-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 






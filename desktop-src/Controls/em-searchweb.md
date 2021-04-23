---
title: Сообщение EM_SEARCHWEB (Коммктрл. h)
description: Открывает браузер и выполняет поиск в Интернете с выбранным текстом в качестве условия поиска.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Элементы управления Windows для EM_SEARCHWEB сообщений
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892394"
---
# <a name="em_searchweb-message"></a><span data-ttu-id="b355a-104">\_Сообщение СЕАРЧВЕБ EM</span><span class="sxs-lookup"><span data-stu-id="b355a-104">EM\_SEARCHWEB message</span></span>

<span data-ttu-id="b355a-105">Открывает браузер и выполняет поиск в Интернете с выбранным текстом в качестве условия поиска.</span><span class="sxs-lookup"><span data-stu-id="b355a-105">Opens the browser and performs a web search with the selected text as the search term.</span></span>

## <a name="parameters"></a><span data-ttu-id="b355a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b355a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b355a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b355a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b355a-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b355a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b355a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b355a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b355a-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b355a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b355a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b355a-111">Return value</span></span>

<span data-ttu-id="b355a-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b355a-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b355a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b355a-113">Remarks</span></span>

<span data-ttu-id="b355a-114">Если функция "Поиск в Интернете" отключена с помощью сообщения [**EM \_ енаблесеарчвеб**](em-enablesearchweb.md) , это сообщение не действует.</span><span class="sxs-lookup"><span data-stu-id="b355a-114">If the "Search the web" feature is disabled using the [**EM\_ENABLESEARCHWEB**](em-enablesearchweb.md) message, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b355a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b355a-115">Requirements</span></span>



| <span data-ttu-id="b355a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b355a-116">Requirement</span></span> | <span data-ttu-id="b355a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b355a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b355a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b355a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b355a-119">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="b355a-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b355a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b355a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b355a-121">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="b355a-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b355a-122">Header</span><span class="sxs-lookup"><span data-stu-id="b355a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b355a-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b355a-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b355a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b355a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b355a-125">**EM \_ енаблесеарчвеб**</span><span class="sxs-lookup"><span data-stu-id="b355a-125">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> </dl>

 

 






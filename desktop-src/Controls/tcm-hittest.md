---
title: Сообщение TCM_HITTEST (Коммктрл. h)
description: Определяет, какая вкладка, если она есть, находится на заданной позиции экрана. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Элементы управления Windows для TCM_HITTEST сообщений
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654666"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="02511-105">\_Сообщение HITTEST TCM</span><span class="sxs-lookup"><span data-stu-id="02511-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="02511-106">Определяет, какая вкладка, если она есть, находится на заданной позиции экрана.</span><span class="sxs-lookup"><span data-stu-id="02511-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="02511-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .</span><span class="sxs-lookup"><span data-stu-id="02511-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="02511-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="02511-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02511-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02511-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="02511-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="02511-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="02511-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02511-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02511-112">Указатель на структуру [**тчиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) , указывающую, на какой позиции экрана нужно выполнить проверку.</span><span class="sxs-lookup"><span data-stu-id="02511-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02511-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02511-113">Return value</span></span>

<span data-ttu-id="02511-114">Возвращает индекс вкладки или значение-1, если вкладка не находится в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="02511-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="02511-115">Требования</span><span class="sxs-lookup"><span data-stu-id="02511-115">Requirements</span></span>



| <span data-ttu-id="02511-116">Требование</span><span class="sxs-lookup"><span data-stu-id="02511-116">Requirement</span></span> | <span data-ttu-id="02511-117">Значение</span><span class="sxs-lookup"><span data-stu-id="02511-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02511-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02511-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02511-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02511-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02511-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02511-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02511-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02511-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02511-122">Header</span><span class="sxs-lookup"><span data-stu-id="02511-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02511-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="02511-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






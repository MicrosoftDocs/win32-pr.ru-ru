---
title: Сообщение TCM_GETCURSEL (Коммктрл. h)
description: Определяет текущую выбранную вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Элементы управления Windows для TCM_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654670"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="fc877-105">\_Сообщение TCM</span><span class="sxs-lookup"><span data-stu-id="fc877-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="fc877-106">Определяет текущую выбранную вкладку в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="fc877-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="fc877-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="fc877-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc877-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc877-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc877-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc877-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc877-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fc877-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc877-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc877-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fc877-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fc877-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc877-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc877-113">Return value</span></span>

<span data-ttu-id="fc877-114">Возвращает индекс выбранной вкладки, если она выполнена успешно, или значение-1, если вкладка не выбрана.</span><span class="sxs-lookup"><span data-stu-id="fc877-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc877-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fc877-115">Requirements</span></span>



| <span data-ttu-id="fc877-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fc877-116">Requirement</span></span> | <span data-ttu-id="fc877-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fc877-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc877-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc877-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc877-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc877-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc877-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc877-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc877-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc877-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc877-122">Header</span><span class="sxs-lookup"><span data-stu-id="fc877-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc877-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc877-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Сообщение TCM_SETMINTABWIDTH (Коммктрл. h)
description: Устанавливает минимальную ширину элементов в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетминтабвидс.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Элементы управления Windows для TCM_SETMINTABWIDTH сообщений
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654414"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="52fd2-105">\_Сообщение СЕТМИНТАБВИДС TCM</span><span class="sxs-lookup"><span data-stu-id="52fd2-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="52fd2-106">Устанавливает минимальную ширину элементов в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="52fd2-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="52fd2-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетминтабвидс**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .</span><span class="sxs-lookup"><span data-stu-id="52fd2-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="52fd2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52fd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52fd2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52fd2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="52fd2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="52fd2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="52fd2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52fd2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52fd2-112">Минимальная ширина, устанавливаемая для элемента управления вкладки.</span><span class="sxs-lookup"><span data-stu-id="52fd2-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="52fd2-113">Если этот параметр имеет значение-1, то элемент управления будет использовать ширину табуляции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52fd2-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52fd2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52fd2-114">Return value</span></span>

<span data-ttu-id="52fd2-115">Возвращает значение типа INT, представляющее предыдущую минимальную ширину табуляции.</span><span class="sxs-lookup"><span data-stu-id="52fd2-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="52fd2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="52fd2-116">Requirements</span></span>



| <span data-ttu-id="52fd2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="52fd2-117">Requirement</span></span> | <span data-ttu-id="52fd2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="52fd2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52fd2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52fd2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52fd2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52fd2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52fd2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52fd2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52fd2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52fd2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52fd2-123">Header</span><span class="sxs-lookup"><span data-stu-id="52fd2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52fd2-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fd2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






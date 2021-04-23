---
title: Сообщение TDM_SET_PROGRESS_BAR_POS (Коммктрл. h)
description: Задает расположение индикатора выполнения в диалоговом окне задачи.
ms.assetid: 82247d70-8527-4195-87af-5c4e5fd1d1a2
keywords:
- Элементы управления Windows для TDM_SET_PROGRESS_BAR_POS сообщений
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_POS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58e12b67c218f21c72f28089a3246d52c6165740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489012"
---
# <a name="tdm_set_progress_bar_pos-message"></a><span data-ttu-id="001f8-104">TDM \_ Задание \_ индикатора \_ выполнения \_ сообщение POS</span><span class="sxs-lookup"><span data-stu-id="001f8-104">TDM\_SET\_PROGRESS\_BAR\_POS message</span></span>

<span data-ttu-id="001f8-105">Задает расположение индикатора выполнения в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="001f8-105">Sets the position of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="001f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="001f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="001f8-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="001f8-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001f8-108">Значение **типа int** , указывающее новую точку.</span><span class="sxs-lookup"><span data-stu-id="001f8-108">An **int** that specifies the new position.</span></span>

</dd> <dt>

<span data-ttu-id="001f8-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="001f8-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001f8-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="001f8-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="001f8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="001f8-111">Return value</span></span>

<span data-ttu-id="001f8-112">Возвращает предыдущее расположение.</span><span class="sxs-lookup"><span data-stu-id="001f8-112">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="001f8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="001f8-113">Requirements</span></span>



| <span data-ttu-id="001f8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="001f8-114">Requirement</span></span> | <span data-ttu-id="001f8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="001f8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="001f8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="001f8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="001f8-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="001f8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="001f8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="001f8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="001f8-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="001f8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="001f8-120">Header</span><span class="sxs-lookup"><span data-stu-id="001f8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="001f8-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="001f8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






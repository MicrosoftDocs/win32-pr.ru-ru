---
title: Сообщение TCM_GETROWCOUNT (Коммктрл. h)
description: Извлекает текущее число строк вкладок в элементе управления "Вкладка". Это сообщение можно отправить явно или с помощью \_ макроса табктрл.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Элементы управления Windows для TCM_GETROWCOUNT сообщений
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892530"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="d182f-105">\_Сообщение TCM ROWCOUNT</span><span class="sxs-lookup"><span data-stu-id="d182f-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="d182f-106">Извлекает текущее число строк вкладок в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="d182f-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="d182f-107">Это сообщение можно отправить явно или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .</span><span class="sxs-lookup"><span data-stu-id="d182f-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d182f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d182f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d182f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d182f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d182f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d182f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d182f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d182f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d182f-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d182f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d182f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d182f-113">Return value</span></span>

<span data-ttu-id="d182f-114">Возвращает число строк вкладок.</span><span class="sxs-lookup"><span data-stu-id="d182f-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d182f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d182f-115">Remarks</span></span>

<span data-ttu-id="d182f-116">Только элементы управления "Вкладка", имеющие [**\_ Многострочный стиль TCS**](tab-control-styles.md) , могут содержать несколько строк вкладок.</span><span class="sxs-lookup"><span data-stu-id="d182f-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d182f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d182f-117">Requirements</span></span>



| <span data-ttu-id="d182f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d182f-118">Requirement</span></span> | <span data-ttu-id="d182f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d182f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d182f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d182f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d182f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d182f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d182f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d182f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d182f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d182f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d182f-124">Header</span><span class="sxs-lookup"><span data-stu-id="d182f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d182f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d182f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






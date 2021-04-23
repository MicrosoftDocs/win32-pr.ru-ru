---
title: Сообщение TTM_GETTITLE (Коммктрл. h)
description: Получение сведений, касающихся заголовка элемента управления ToolTip.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- Элементы управления Windows для TTM_GETTITLE сообщений
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988673"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="876d1-104">\_Сообщение ТТМ</span><span class="sxs-lookup"><span data-stu-id="876d1-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="876d1-105">Получение сведений, касающихся заголовка элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="876d1-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="876d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="876d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="876d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="876d1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="876d1-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="876d1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="876d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="876d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="876d1-110">Указатель на структуру [**ттжеттитле**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) , содержащую сведения о заголовке подсказки.</span><span class="sxs-lookup"><span data-stu-id="876d1-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="876d1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="876d1-111">Return value</span></span>

<span data-ttu-id="876d1-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="876d1-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="876d1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="876d1-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="876d1-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="876d1-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="876d1-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="876d1-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="876d1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="876d1-116">Requirements</span></span>



| <span data-ttu-id="876d1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="876d1-117">Requirement</span></span> | <span data-ttu-id="876d1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="876d1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="876d1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="876d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="876d1-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="876d1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="876d1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="876d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="876d1-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="876d1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="876d1-123">Header</span><span class="sxs-lookup"><span data-stu-id="876d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="876d1-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="876d1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






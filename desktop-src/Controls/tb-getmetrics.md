---
title: Сообщение TB_GETMETRICS (Коммктрл. h)
description: Извлекает метрики элемента управления ToolBar.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- Элементы управления Windows для TB_GETMETRICS сообщений
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892341"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="1c00f-104">\_Сообщение о НЕметриках ТБ</span><span class="sxs-lookup"><span data-stu-id="1c00f-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="1c00f-105">Извлекает метрики элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="1c00f-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c00f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c00f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c00f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c00f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1c00f-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1c00f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1c00f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c00f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c00f-110">Указатель на структуру [**тбметрикс**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) , которая получает метрики панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1c00f-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c00f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c00f-111">Return value</span></span>

<span data-ttu-id="1c00f-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="1c00f-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c00f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c00f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c00f-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="1c00f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1c00f-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1c00f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c00f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1c00f-116">Requirements</span></span>



| <span data-ttu-id="1c00f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1c00f-117">Requirement</span></span> | <span data-ttu-id="1c00f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1c00f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c00f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c00f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c00f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c00f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c00f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c00f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c00f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c00f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c00f-123">Header</span><span class="sxs-lookup"><span data-stu-id="1c00f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c00f-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c00f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






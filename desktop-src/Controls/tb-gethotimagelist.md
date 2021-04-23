---
title: Сообщение TB_GETHOTIMAGELIST (Коммктрл. h)
description: Извлекает список изображений, используемый элементом управления Toolbar для показа кнопок.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Элементы управления Windows для TB_GETHOTIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136131"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="d3843-104">\_Сообщение ЖЕСОТИМАЖЕЛИСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="d3843-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="d3843-105">Извлекает список изображений, используемый элементом управления Toolbar для показа кнопок.</span><span class="sxs-lookup"><span data-stu-id="d3843-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3843-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3843-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3843-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3843-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d3843-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d3843-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d3843-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3843-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d3843-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d3843-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3843-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3843-111">Return value</span></span>

<span data-ttu-id="d3843-112">Возвращает указатель на список изображений, используемый элементом управления для показа активных кнопок, или **значение NULL** , если список горячих образов не задан.</span><span class="sxs-lookup"><span data-stu-id="d3843-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3843-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3843-113">Remarks</span></span>

<span data-ttu-id="d3843-114">Кнопка находится в активном положении при наведении на нее курсора.</span><span class="sxs-lookup"><span data-stu-id="d3843-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="d3843-115">Элементы управления "панель инструментов" должны иметь [**стиль \_ списка**](toolbar-control-and-button-styles.md) [**тбстиле \_ Flat**](toolbar-control-and-button-styles.md) или тбстиле, чтобы иметь активные элементы.</span><span class="sxs-lookup"><span data-stu-id="d3843-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3843-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d3843-116">Requirements</span></span>



| <span data-ttu-id="d3843-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d3843-117">Requirement</span></span> | <span data-ttu-id="d3843-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d3843-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3843-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3843-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3843-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3843-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3843-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3843-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3843-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3843-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3843-123">Header</span><span class="sxs-lookup"><span data-stu-id="d3843-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3843-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3843-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






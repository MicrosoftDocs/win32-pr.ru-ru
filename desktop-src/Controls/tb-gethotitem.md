---
title: Сообщение TB_GETHOTITEM (Коммктрл. h)
description: Получает индекс горячего элемента на панели инструментов.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- Элементы управления Windows для TB_GETHOTITEM сообщений
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490194"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="adc40-104">\_Сообщение ЖЕСОТИТЕМ ТБ</span><span class="sxs-lookup"><span data-stu-id="adc40-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="adc40-105">Получает индекс горячего элемента на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="adc40-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="adc40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adc40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc40-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="adc40-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="adc40-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="adc40-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="adc40-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="adc40-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="adc40-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="adc40-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc40-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adc40-111">Return value</span></span>

<span data-ttu-id="adc40-112">Возвращает индекс горячего элемента или значение-1, если не задан ни один активный элемент.</span><span class="sxs-lookup"><span data-stu-id="adc40-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="adc40-113">Элементы управления ToolBar, у которых нет [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) , не имеют активных элементов.</span><span class="sxs-lookup"><span data-stu-id="adc40-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc40-114">Требования</span><span class="sxs-lookup"><span data-stu-id="adc40-114">Requirements</span></span>



| <span data-ttu-id="adc40-115">Требование</span><span class="sxs-lookup"><span data-stu-id="adc40-115">Requirement</span></span> | <span data-ttu-id="adc40-116">Значение</span><span class="sxs-lookup"><span data-stu-id="adc40-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adc40-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adc40-117">Minimum supported client</span></span><br/> | <span data-ttu-id="adc40-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adc40-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="adc40-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adc40-119">Minimum supported server</span></span><br/> | <span data-ttu-id="adc40-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="adc40-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="adc40-121">Header</span><span class="sxs-lookup"><span data-stu-id="adc40-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="adc40-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="adc40-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Сообщение TB_SETHOTITEM (Коммктрл. h)
description: Задает горячий элемент на панели инструментов.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Элементы управления Windows для TB_SETHOTITEM сообщений
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892333"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="63159-104">\_Сообщение СЕСОТИТЕМ ТБ</span><span class="sxs-lookup"><span data-stu-id="63159-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="63159-105">Задает горячий элемент на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="63159-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="63159-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63159-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63159-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63159-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63159-108">Индекс элемента, который будет активным.</span><span class="sxs-lookup"><span data-stu-id="63159-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="63159-109">Если это значение равно-1, ни один из элементов не будет активным.</span><span class="sxs-lookup"><span data-stu-id="63159-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="63159-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63159-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="63159-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="63159-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63159-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63159-112">Return value</span></span>

<span data-ttu-id="63159-113">Возвращает индекс предыдущего горячего элемента или значение-1, если элемент не был активным.</span><span class="sxs-lookup"><span data-stu-id="63159-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="63159-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63159-114">Remarks</span></span>

<span data-ttu-id="63159-115">Поведение этого сообщения не определено для панелей инструментов, не имеющих [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="63159-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="63159-116">Требования</span><span class="sxs-lookup"><span data-stu-id="63159-116">Requirements</span></span>



| <span data-ttu-id="63159-117">Требование</span><span class="sxs-lookup"><span data-stu-id="63159-117">Requirement</span></span> | <span data-ttu-id="63159-118">Значение</span><span class="sxs-lookup"><span data-stu-id="63159-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63159-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63159-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63159-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63159-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63159-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63159-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63159-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63159-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63159-123">Header</span><span class="sxs-lookup"><span data-stu-id="63159-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63159-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="63159-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






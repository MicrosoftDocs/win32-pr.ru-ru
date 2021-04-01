---
title: Сообщение TB_ISBUTTONHIGHLIGHTED (Коммктрл. h)
description: Проверяет состояние выделения кнопки на панели инструментов.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- Элементы управления Windows для TB_ISBUTTONHIGHLIGHTED сообщений
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071380"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="f5816-104">\_Сообщение ИСБУТТОНХИГХЛИГХТЕД ТБ</span><span class="sxs-lookup"><span data-stu-id="f5816-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="f5816-105">Проверяет состояние выделения кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="f5816-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5816-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5816-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5816-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5816-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5816-108">Идентификатор команды для кнопки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="f5816-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="f5816-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5816-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f5816-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f5816-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5816-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5816-111">Return value</span></span>

<span data-ttu-id="f5816-112">Возвращает ненулевое значение, если кнопка выделяется, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f5816-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5816-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f5816-113">Requirements</span></span>



| <span data-ttu-id="f5816-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f5816-114">Requirement</span></span> | <span data-ttu-id="f5816-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5816-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5816-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5816-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5816-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5816-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5816-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5816-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5816-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5816-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5816-120">Header</span><span class="sxs-lookup"><span data-stu-id="f5816-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5816-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5816-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Сообщение TB_ISBUTTONHIDDEN (Коммктрл. h)
description: Определяет, скрыта ли указанная кнопка на панели инструментов.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- Элементы управления Windows для TB_ISBUTTONHIDDEN сообщений
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989435"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="da5d3-104">\_Сообщение ИСБУТТОНХИДДЕН ТБ</span><span class="sxs-lookup"><span data-stu-id="da5d3-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="da5d3-105">Определяет, скрыта ли указанная кнопка на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="da5d3-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="da5d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da5d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da5d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da5d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da5d3-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="da5d3-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="da5d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da5d3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="da5d3-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="da5d3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da5d3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da5d3-111">Return value</span></span>

<span data-ttu-id="da5d3-112">Возвращает ненулевое значение, если кнопка скрыта, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="da5d3-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="da5d3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="da5d3-113">Requirements</span></span>



| <span data-ttu-id="da5d3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="da5d3-114">Requirement</span></span> | <span data-ttu-id="da5d3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da5d3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da5d3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da5d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da5d3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da5d3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da5d3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da5d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da5d3-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da5d3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da5d3-120">Header</span><span class="sxs-lookup"><span data-stu-id="da5d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da5d3-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="da5d3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






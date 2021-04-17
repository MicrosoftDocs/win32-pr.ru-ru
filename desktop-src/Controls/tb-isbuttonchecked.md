---
title: Сообщение TB_ISBUTTONCHECKED (Коммктрл. h)
description: Определяет, проверяется ли указанная кнопка на панели инструментов.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- Элементы управления Windows для TB_ISBUTTONCHECKED сообщений
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb9bc573478ea55ce8e0bda48ff16679b135fc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533977"
---
# <a name="tb_isbuttonchecked-message"></a><span data-ttu-id="a445c-104">\_Сообщение ИСБУТТОНЧЕККЕД ТБ</span><span class="sxs-lookup"><span data-stu-id="a445c-104">TB\_ISBUTTONCHECKED message</span></span>

<span data-ttu-id="a445c-105">Определяет, проверяется ли указанная кнопка на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="a445c-105">Determines whether the specified button in a toolbar is checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="a445c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a445c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a445c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a445c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a445c-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="a445c-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="a445c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a445c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a445c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a445c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a445c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a445c-111">Return value</span></span>

<span data-ttu-id="a445c-112">Возвращает ненулевое значение, если кнопка отмечена, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a445c-112">Returns nonzero if the button is checked, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a445c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a445c-113">Requirements</span></span>



| <span data-ttu-id="a445c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a445c-114">Requirement</span></span> | <span data-ttu-id="a445c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a445c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a445c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a445c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a445c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a445c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a445c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a445c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a445c-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a445c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a445c-120">Header</span><span class="sxs-lookup"><span data-stu-id="a445c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a445c-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a445c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






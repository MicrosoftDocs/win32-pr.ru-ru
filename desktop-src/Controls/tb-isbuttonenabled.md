---
title: Сообщение TB_ISBUTTONENABLED (Коммктрл. h)
description: Определяет, включена ли указанная кнопка на панели инструментов.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- Элементы управления Windows для TB_ISBUTTONENABLED сообщений
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891701"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="643a0-104">\_Сообщение ИСБУТТОНЕНАБЛЕД ТБ</span><span class="sxs-lookup"><span data-stu-id="643a0-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="643a0-105">Определяет, включена ли указанная кнопка на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="643a0-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="643a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="643a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643a0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="643a0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="643a0-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="643a0-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="643a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="643a0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="643a0-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="643a0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="643a0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="643a0-111">Return value</span></span>

<span data-ttu-id="643a0-112">Возвращает ненулевое значение, если кнопка включена, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="643a0-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="643a0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="643a0-113">Requirements</span></span>



| <span data-ttu-id="643a0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="643a0-114">Requirement</span></span> | <span data-ttu-id="643a0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="643a0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="643a0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="643a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="643a0-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="643a0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="643a0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="643a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="643a0-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="643a0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="643a0-120">Header</span><span class="sxs-lookup"><span data-stu-id="643a0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="643a0-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="643a0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Сообщение TB_ISBUTTONPRESSED (Коммктрл. h)
description: Определяет, нажата ли указанная кнопка на панели инструментов.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- Элементы управления Windows для TB_ISBUTTONPRESSED сообщений
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135459"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="e1ed5-104">\_Сообщение ИСБУТТОНПРЕССЕД ТБ</span><span class="sxs-lookup"><span data-stu-id="e1ed5-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="e1ed5-105">Определяет, нажата ли указанная кнопка на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="e1ed5-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1ed5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ed5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ed5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1ed5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1ed5-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="e1ed5-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="e1ed5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1ed5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e1ed5-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e1ed5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ed5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1ed5-111">Return value</span></span>

<span data-ttu-id="e1ed5-112">Возвращает ненулевое значение, если кнопка нажата, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e1ed5-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ed5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e1ed5-113">Requirements</span></span>



| <span data-ttu-id="e1ed5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e1ed5-114">Requirement</span></span> | <span data-ttu-id="e1ed5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e1ed5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ed5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1ed5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ed5-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1ed5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1ed5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1ed5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ed5-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1ed5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1ed5-120">Header</span><span class="sxs-lookup"><span data-stu-id="e1ed5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ed5-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ed5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






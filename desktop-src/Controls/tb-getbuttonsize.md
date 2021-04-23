---
title: Сообщение TB_GETBUTTONSIZE (Коммктрл. h)
description: Извлекает текущую ширину и высоту кнопок панели инструментов в пикселях.
ms.assetid: c1b72494-670b-4cf8-a78f-c67b6eee0677
keywords:
- Элементы управления Windows для TB_GETBUTTONSIZE сообщений
topic_type:
- apiref
api_name:
- TB_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a414f5b338353d7d8ce22a081e9b711a2b56a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892798"
---
# <a name="tb_getbuttonsize-message"></a><span data-ttu-id="71b70-104">\_Сообщение ЖЕТБУТТОНСИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="71b70-104">TB\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="71b70-105">Извлекает текущую ширину и высоту кнопок панели инструментов в пикселях.</span><span class="sxs-lookup"><span data-stu-id="71b70-105">Retrieves the current width and height of toolbar buttons, in pixels.</span></span>

## <a name="parameters"></a><span data-ttu-id="71b70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71b70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71b70-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="71b70-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="71b70-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="71b70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71b70-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="71b70-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="71b70-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b70-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71b70-111">Return value</span></span>

<span data-ttu-id="71b70-112">Возвращает значение **типа DWORD** , содержащее значения ширины и высоты в нижнем слове и верхнем слове соответственно.</span><span class="sxs-lookup"><span data-stu-id="71b70-112">Returns a **DWORD** value that contains the width and height values in the low word and high word, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b70-113">Требования</span><span class="sxs-lookup"><span data-stu-id="71b70-113">Requirements</span></span>



| <span data-ttu-id="71b70-114">Требование</span><span class="sxs-lookup"><span data-stu-id="71b70-114">Requirement</span></span> | <span data-ttu-id="71b70-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71b70-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71b70-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71b70-116">Minimum supported client</span></span><br/> | <span data-ttu-id="71b70-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71b70-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71b70-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71b70-118">Minimum supported server</span></span><br/> | <span data-ttu-id="71b70-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71b70-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71b70-120">Header</span><span class="sxs-lookup"><span data-stu-id="71b70-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b70-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b70-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






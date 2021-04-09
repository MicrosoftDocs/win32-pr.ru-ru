---
title: Сообщение TB_GETSTATE (Коммктрл. h)
description: Получает сведения о состоянии указанной кнопки на панели инструментов, такие как включение, нажатие или проверка.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Элементы управления Windows для TB_GETSTATE сообщений
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891598"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="20c4f-104">\_Сообщение о состоянии ТБ</span><span class="sxs-lookup"><span data-stu-id="20c4f-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="20c4f-105">Получает сведения о состоянии указанной кнопки на панели инструментов, такие как включение, нажатие или проверка.</span><span class="sxs-lookup"><span data-stu-id="20c4f-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="20c4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20c4f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20c4f-108">Идентификатор команды для получения сведений.</span><span class="sxs-lookup"><span data-stu-id="20c4f-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="20c4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20c4f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="20c4f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="20c4f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c4f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20c4f-111">Return value</span></span>

<span data-ttu-id="20c4f-112">Возвращает сведения о состоянии кнопки, если они успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="20c4f-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="20c4f-113">Сведения о состоянии кнопки могут представлять собой сочетание значений, перечисленных в поле [**состояния кнопки на панели инструментов**](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="20c4f-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20c4f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="20c4f-114">Requirements</span></span>



| <span data-ttu-id="20c4f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="20c4f-115">Requirement</span></span> | <span data-ttu-id="20c4f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="20c4f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20c4f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20c4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20c4f-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20c4f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20c4f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20c4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20c4f-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20c4f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20c4f-121">Header</span><span class="sxs-lookup"><span data-stu-id="20c4f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="20c4f-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="20c4f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






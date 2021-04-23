---
title: Сообщение TB_SETLISTGAP (Коммктрл. h)
description: Задает расстояние между кнопками панели инструментов на определенной панели инструментов.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Элементы управления Windows для TB_SETLISTGAP сообщений
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891405"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="69d27-104">\_Сообщение СЕТЛИСТГАП ТБ</span><span class="sxs-lookup"><span data-stu-id="69d27-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="69d27-105">Задает расстояние между кнопками панели инструментов на определенной панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="69d27-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="69d27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69d27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d27-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69d27-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69d27-108">Зазор (в пикселях) между кнопками на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="69d27-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="69d27-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69d27-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69d27-110">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="69d27-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d27-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69d27-111">Return value</span></span>

<span data-ttu-id="69d27-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="69d27-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d27-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69d27-113">Remarks</span></span>

<span data-ttu-id="69d27-114">Разрыв между кнопками применяется только к окну элемента управления ToolBar, которое получает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="69d27-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="69d27-115">Получение этого сообщения запускает перерисовку панели инструментов, если панель инструментов видима в данный момент.</span><span class="sxs-lookup"><span data-stu-id="69d27-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d27-116">Требования</span><span class="sxs-lookup"><span data-stu-id="69d27-116">Requirements</span></span>



| <span data-ttu-id="69d27-117">Требование</span><span class="sxs-lookup"><span data-stu-id="69d27-117">Requirement</span></span> | <span data-ttu-id="69d27-118">Значение</span><span class="sxs-lookup"><span data-stu-id="69d27-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69d27-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69d27-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69d27-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69d27-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69d27-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69d27-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69d27-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69d27-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69d27-123">Header</span><span class="sxs-lookup"><span data-stu-id="69d27-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d27-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d27-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






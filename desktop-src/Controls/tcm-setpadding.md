---
title: Сообщение TCM_SETPADDING (Коммктрл. h)
description: Задает объем пространства (заполнение) вокруг значка и метки каждой вкладки в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетпаддинг.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Элементы управления Windows для TCM_SETPADDING сообщений
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654412"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="d198e-105">\_Сообщение СЕТПАДДИНГ TCM</span><span class="sxs-lookup"><span data-stu-id="d198e-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="d198e-106">Задает объем пространства (заполнение) вокруг значка и метки каждой вкладки в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="d198e-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="d198e-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетпаддинг**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .</span><span class="sxs-lookup"><span data-stu-id="d198e-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d198e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d198e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d198e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d198e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d198e-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это значение **типа int** , определяющее величину отступа по горизонтали (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="d198e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="d198e-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это значение **типа int** , указывающее величину вертикального заполнения (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="d198e-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d198e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d198e-112">Return value</span></span>

<span data-ttu-id="d198e-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d198e-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d198e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d198e-114">Requirements</span></span>



| <span data-ttu-id="d198e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d198e-115">Requirement</span></span> | <span data-ttu-id="d198e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d198e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d198e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d198e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d198e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d198e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d198e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d198e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d198e-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d198e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d198e-121">Header</span><span class="sxs-lookup"><span data-stu-id="d198e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d198e-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d198e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


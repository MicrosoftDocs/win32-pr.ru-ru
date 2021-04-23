---
title: Сообщение TTM_SETTOOLINFO (Коммктрл. h)
description: Задает сведения, которые поддерживаются элементом управления ToolTip для средства.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Элементы управления Windows для TTM_SETTOOLINFO сообщений
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492843"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="7f4db-104">\_Сообщение ТТМ сеттулинфо</span><span class="sxs-lookup"><span data-stu-id="7f4db-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="7f4db-105">Задает сведения, которые поддерживаются элементом управления ToolTip для средства.</span><span class="sxs-lookup"><span data-stu-id="7f4db-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f4db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f4db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f4db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f4db-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7f4db-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7f4db-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7f4db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f4db-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f4db-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , указывающую сведения, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="7f4db-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="7f4db-111">Перед отправкой этого сообщения необходимо задать элемент **кбсизе** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="7f4db-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f4db-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f4db-112">Return value</span></span>

<span data-ttu-id="7f4db-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7f4db-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f4db-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f4db-114">Remarks</span></span>

<span data-ttu-id="7f4db-115">Некоторые внутренние свойства средства устанавливаются при создании средства и не пересчитываются при отправке сообщения **ТТМ \_ сеттулинфо** .</span><span class="sxs-lookup"><span data-stu-id="7f4db-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="7f4db-116">Если вы просто назначаете значения структуре [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) и передаете ее элементу управления ToolTip с помощью сообщения **ТТМ \_ сеттулинфо** , эти свойства могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="7f4db-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="7f4db-117">Вместо этого приложение должно сначала запросить текущую структуру **тулинфо** средства, отправив элемент управления ToolTip в сообщение [**ТТМ \_ жеттулинфо**](ttm-gettoolinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7f4db-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="7f4db-118">Затем измените элементы этой структуры по мере необходимости и передайте ее обратно в элемент управления ToolTip с помощью **ТТМ \_ сеттулинфо**.</span><span class="sxs-lookup"><span data-stu-id="7f4db-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="7f4db-119">При вызове **ТТМ \_ сеттулинфо** строка, на которую указывает элемент **лпсзтекст** структуры [**Тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , не должна превышать 80 **Тчарс** в длину, включая завершающее **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f4db-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f4db-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7f4db-120">Requirements</span></span>



| <span data-ttu-id="7f4db-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7f4db-121">Requirement</span></span> | <span data-ttu-id="7f4db-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7f4db-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4db-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f4db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4db-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f4db-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f4db-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f4db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4db-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f4db-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f4db-127">Header</span><span class="sxs-lookup"><span data-stu-id="7f4db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4db-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f4db-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7f4db-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7f4db-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7f4db-130">**ТТМ \_ СЕТТУЛИНФОВ** (Юникод) и **ТТМ \_ сеттулинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7f4db-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 






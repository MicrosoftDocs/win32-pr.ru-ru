---
title: Сообщение TTM_HITTEST (Коммктрл. h)
description: Проверяет точку, чтобы определить, находится ли она в ограничивающем прямоугольнике указанного инструмента, и, если это так, получает сведения о средстве.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Элементы управления Windows для TTM_HITTEST сообщений
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490674"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="08d0e-104">\_Сообщение ТТМ HITTEST</span><span class="sxs-lookup"><span data-stu-id="08d0e-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="08d0e-105">Проверяет точку, чтобы определить, находится ли она в ограничивающем прямоугольнике указанного инструмента, и, если это так, получает сведения о средстве.</span><span class="sxs-lookup"><span data-stu-id="08d0e-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="08d0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d0e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08d0e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="08d0e-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="08d0e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="08d0e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08d0e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08d0e-110">Указатель на структуру [**тситтестинфо**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) .</span><span class="sxs-lookup"><span data-stu-id="08d0e-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="08d0e-111">При отправке сообщения элемент **HWND** должен задавать дескриптор для инструмента, а элемент **PT** должен указывать координаты точки.</span><span class="sxs-lookup"><span data-stu-id="08d0e-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="08d0e-112">Если возвращаемое значение равно **true**, то элемент **Ti** (структура [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) получает сведения о средстве, занимаемом точкой.</span><span class="sxs-lookup"><span data-stu-id="08d0e-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="08d0e-113">Перед отправкой этого сообщения элемент **кбсизе** структуры **Ti** должен быть заполнен.</span><span class="sxs-lookup"><span data-stu-id="08d0e-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d0e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08d0e-114">Return value</span></span>

<span data-ttu-id="08d0e-115">Возвращает **значение true** , если средство занимает указанную точку, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="08d0e-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d0e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08d0e-116">Remarks</span></span>

<span data-ttu-id="08d0e-117">Это сообщение должно быть отправлено, если для инструмента \_ установлен флаг «Track».</span><span class="sxs-lookup"><span data-stu-id="08d0e-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="08d0e-118">Дополнительные сведения об этом флаге см. в разделе [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span><span class="sxs-lookup"><span data-stu-id="08d0e-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="08d0e-119">ТТМ \_ HITTEST завершится ошибкой \_ , если не задана программа TTF Track, независимо от того, находится ли точка попадания в прямоугольнике инструментов.</span><span class="sxs-lookup"><span data-stu-id="08d0e-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d0e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="08d0e-120">Requirements</span></span>



| <span data-ttu-id="08d0e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="08d0e-121">Requirement</span></span> | <span data-ttu-id="08d0e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="08d0e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08d0e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08d0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="08d0e-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08d0e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08d0e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08d0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="08d0e-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08d0e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08d0e-127">Header</span><span class="sxs-lookup"><span data-stu-id="08d0e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d0e-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d0e-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="08d0e-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="08d0e-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="08d0e-130">**ТТМ \_ ХИТТЕСТВ** (Юникод) и **ТТМ \_ хиттеста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="08d0e-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 






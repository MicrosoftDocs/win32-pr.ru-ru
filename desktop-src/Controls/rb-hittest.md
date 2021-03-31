---
title: Сообщение RB_HITTEST (Коммктрл. h)
description: Определяет, какая часть полосы элементов управления находится в заданной точке экрана, если в этой точке существует полоса главной панели.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Элементы управления Windows для RB_HITTEST сообщений
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071181"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="39ecd-104">\_Сообщение HITTEST RB</span><span class="sxs-lookup"><span data-stu-id="39ecd-104">RB\_HITTEST message</span></span>

<span data-ttu-id="39ecd-105">Определяет, какая часть полосы элементов управления находится в заданной точке экрана, если в этой точке существует полоса главной панели.</span><span class="sxs-lookup"><span data-stu-id="39ecd-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="39ecd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39ecd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ecd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39ecd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="39ecd-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="39ecd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="39ecd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39ecd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39ecd-110">Указатель на структуру [**рбхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="39ecd-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="39ecd-111">Перед отправкой сообщения элемент **PT** этой структуры должен быть инициализирован в точке, которая будет проверена на попадание, в клиентских координатах.</span><span class="sxs-lookup"><span data-stu-id="39ecd-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ecd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39ecd-112">Return value</span></span>

<span data-ttu-id="39ecd-113">Возвращает отсчитываемый от нуля индекс полосы в заданной точке или значение-1, если полоса элементов не находилась в точке.</span><span class="sxs-lookup"><span data-stu-id="39ecd-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ecd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="39ecd-114">Requirements</span></span>



| <span data-ttu-id="39ecd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="39ecd-115">Requirement</span></span> | <span data-ttu-id="39ecd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="39ecd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39ecd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39ecd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39ecd-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39ecd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39ecd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39ecd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39ecd-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39ecd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39ecd-121">Header</span><span class="sxs-lookup"><span data-stu-id="39ecd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ecd-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ecd-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






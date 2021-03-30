---
title: Сообщение HDM_HITTEST (Коммктрл. h)
description: Проверяет точку, чтобы определить, какой элемент заголовка, если таковой имеется, находится в указанной точке.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Элементы управления Windows для HDM_HITTEST сообщений
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136434"
---
# <a name="hdm_hittest-message"></a><span data-ttu-id="ea5c2-104">\_Сообщение HITTEST HDM</span><span class="sxs-lookup"><span data-stu-id="ea5c2-104">HDM\_HITTEST message</span></span>

<span data-ttu-id="ea5c2-105">Проверяет точку, чтобы определить, какой элемент заголовка, если таковой имеется, находится в указанной точке.</span><span class="sxs-lookup"><span data-stu-id="ea5c2-105">Tests a point to determine which header item, if any, is at the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea5c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea5c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea5c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea5c2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea5c2-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ea5c2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea5c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea5c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea5c2-110">Указатель на структуру [**хдхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) , которая содержит позиции для проверки и получает сведения о результатах теста.</span><span class="sxs-lookup"><span data-stu-id="ea5c2-110">A pointer to an [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) structure that contains the position to test and receives information about the results of the test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea5c2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea5c2-111">Return value</span></span>

<span data-ttu-id="ea5c2-112">Возвращает индекс элемента в указанной позиции, если таковой имеется, или значение 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ea5c2-112">Returns the index of the item at the specified position, if any, or   1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea5c2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ea5c2-113">Requirements</span></span>



| <span data-ttu-id="ea5c2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ea5c2-114">Requirement</span></span> | <span data-ttu-id="ea5c2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ea5c2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea5c2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea5c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea5c2-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea5c2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea5c2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea5c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea5c2-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea5c2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea5c2-120">Header</span><span class="sxs-lookup"><span data-stu-id="ea5c2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea5c2-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea5c2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






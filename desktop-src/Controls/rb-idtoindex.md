---
title: Сообщение RB_IDTOINDEX (Коммктрл. h)
description: Преобразует идентификатор диапазона в индекс диапазона в элементе управления главной панели.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- Элементы управления Windows для RB_IDTOINDEX сообщений
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489237"
---
# <a name="rb_idtoindex-message"></a><span data-ttu-id="a8b69-104">\_Сообщение ИДТОИНДЕКС RB</span><span class="sxs-lookup"><span data-stu-id="a8b69-104">RB\_IDTOINDEX message</span></span>

<span data-ttu-id="a8b69-105">Преобразует идентификатор диапазона в индекс диапазона в элементе управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="a8b69-105">Converts a band identifier to a band index in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8b69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8b69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b69-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8b69-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b69-108">Определяемый приложением идентификатор рассматриваемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="a8b69-108">The application-defined identifier of the band in question.</span></span> <span data-ttu-id="a8b69-109">Это значение, передаваемое члену **WID** структуры [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) при вставке полосы.</span><span class="sxs-lookup"><span data-stu-id="a8b69-109">This is the value that was passed in the **wID** member of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure when the band was inserted.</span></span>

</dd> <dt>

<span data-ttu-id="a8b69-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8b69-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a8b69-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a8b69-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b69-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8b69-112">Return value</span></span>

<span data-ttu-id="a8b69-113">Возвращает индекс полосы с отсчетом от нуля в случае успеха или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a8b69-113">Returns the zero-based band index if successful, or -1 otherwise.</span></span> <span data-ttu-id="a8b69-114">При наличии повторяющихся идентификаторов диапазонов возвращается первый из них.</span><span class="sxs-lookup"><span data-stu-id="a8b69-114">If duplicate band identifiers exist, the first one is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b69-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b69-115">Requirements</span></span>



| <span data-ttu-id="a8b69-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b69-116">Requirement</span></span> | <span data-ttu-id="a8b69-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b69-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b69-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8b69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b69-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8b69-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8b69-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8b69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b69-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8b69-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8b69-122">Header</span><span class="sxs-lookup"><span data-stu-id="a8b69-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b69-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b69-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






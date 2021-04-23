---
title: Сообщение RB_DELETEBAND (Коммктрл. h)
description: Удаляет полосу из элемента управления главной панели.
ms.assetid: 15f2ea78-5c3f-4fe1-a020-025c33f00703
keywords:
- Элементы управления Windows для RB_DELETEBAND сообщений
topic_type:
- apiref
api_name:
- RB_DELETEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fd8593c816b64f0d7f82058b3779f256dd521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654568"
---
# <a name="rb_deleteband-message"></a><span data-ttu-id="d1e8a-104">\_Сообщение ДЕЛЕТЕБАНД RB</span><span class="sxs-lookup"><span data-stu-id="d1e8a-104">RB\_DELETEBAND message</span></span>

<span data-ttu-id="d1e8a-105">Удаляет полосу из элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-105">Deletes a band from a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1e8a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1e8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e8a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1e8a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1e8a-108">Отсчитываемый от нуля индекс удаляемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-108">Zero-based index of the band to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1e8a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1e8a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e8a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1e8a-111">Return value</span></span>

<span data-ttu-id="d1e8a-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e8a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d1e8a-113">Requirements</span></span>



| <span data-ttu-id="d1e8a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d1e8a-114">Requirement</span></span> | <span data-ttu-id="d1e8a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d1e8a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e8a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1e8a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e8a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1e8a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1e8a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1e8a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e8a-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1e8a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1e8a-120">Header</span><span class="sxs-lookup"><span data-stu-id="d1e8a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e8a-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e8a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






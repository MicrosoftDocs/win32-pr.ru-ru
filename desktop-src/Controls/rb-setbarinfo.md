---
title: Сообщение RB_SETBARINFO (Коммктрл. h)
description: Задает характеристики элемента управления главной панели.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- Элементы управления Windows для RB_SETBARINFO сообщений
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071178"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="3a3ef-104">\_Сообщение СЕТБАРИНФО RB</span><span class="sxs-lookup"><span data-stu-id="3a3ef-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="3a3ef-105">Задает характеристики элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a3ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a3ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a3ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a3ef-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a3ef-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a3ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a3ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a3ef-110">Указатель на структуру [**ребаринфо**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) , содержащую данные, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="3a3ef-111">Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(ребаринфо).</span><span class="sxs-lookup"><span data-stu-id="3a3ef-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a3ef-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a3ef-112">Return value</span></span>

<span data-ttu-id="3a3ef-113">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a3ef-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3a3ef-114">Requirements</span></span>



| <span data-ttu-id="3a3ef-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3a3ef-115">Requirement</span></span> | <span data-ttu-id="3a3ef-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3a3ef-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a3ef-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a3ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3a3ef-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a3ef-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a3ef-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a3ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3a3ef-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a3ef-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a3ef-121">Header</span><span class="sxs-lookup"><span data-stu-id="3a3ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a3ef-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a3ef-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






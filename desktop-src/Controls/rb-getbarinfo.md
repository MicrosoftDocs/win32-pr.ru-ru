---
title: Сообщение RB_GETBARINFO (Коммктрл. h)
description: Извлекает сведения об элементе управления "Главная панель" и используемом в нем списке изображений.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Элементы управления Windows для RB_GETBARINFO сообщений
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071809"
---
# <a name="rb_getbarinfo-message"></a><span data-ttu-id="2ff04-104">\_Сообщение ЖЕТБАРИНФО RB</span><span class="sxs-lookup"><span data-stu-id="2ff04-104">RB\_GETBARINFO message</span></span>

<span data-ttu-id="2ff04-105">Извлекает сведения об элементе управления "Главная панель" и используемом в нем списке изображений.</span><span class="sxs-lookup"><span data-stu-id="2ff04-105">Retrieves information about the rebar control and the image list it uses.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ff04-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ff04-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2ff04-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2ff04-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2ff04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ff04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff04-110">Указатель на структуру [**ребаринфо**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) , которая будет принимать сведения об элементе управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="2ff04-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that will receive the rebar control information.</span></span> <span data-ttu-id="2ff04-111">Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(ребаринфо).</span><span class="sxs-lookup"><span data-stu-id="2ff04-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff04-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff04-112">Return value</span></span>

<span data-ttu-id="2ff04-113">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2ff04-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff04-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2ff04-114">Requirements</span></span>



| <span data-ttu-id="2ff04-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2ff04-115">Requirement</span></span> | <span data-ttu-id="2ff04-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2ff04-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff04-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ff04-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff04-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ff04-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ff04-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ff04-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff04-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ff04-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ff04-121">Header</span><span class="sxs-lookup"><span data-stu-id="2ff04-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ff04-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff04-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






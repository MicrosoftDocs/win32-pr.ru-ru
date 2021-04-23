---
title: Сообщение RB_GETDROPTARGET (Коммктрл. h)
description: Извлекает указатель интерфейса интерфейс IDropTarget элемента управления "Главная панель".
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Элементы управления Windows для RB_GETDROPTARGET сообщений
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491763"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="cadeb-104">\_Сообщение ЖЕТДРОПТАРЖЕТ RB</span><span class="sxs-lookup"><span data-stu-id="cadeb-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="cadeb-105">Извлекает указатель интерфейса [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) элемента управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="cadeb-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="cadeb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cadeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cadeb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cadeb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cadeb-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cadeb-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cadeb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cadeb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cadeb-110">Указатель на указатель [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) , получающий указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cadeb-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="cadeb-111">Вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с этим указателем, когда он больше не нужен, является обязанностью вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="cadeb-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cadeb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cadeb-112">Return value</span></span>

<span data-ttu-id="cadeb-113">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="cadeb-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cadeb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cadeb-114">Requirements</span></span>



| <span data-ttu-id="cadeb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cadeb-115">Requirement</span></span> | <span data-ttu-id="cadeb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cadeb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cadeb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cadeb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cadeb-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cadeb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cadeb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cadeb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cadeb-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cadeb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cadeb-121">Header</span><span class="sxs-lookup"><span data-stu-id="cadeb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cadeb-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cadeb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


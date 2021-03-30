---
title: Сообщение TB_GETOBJECT (Коммктрл. h)
description: Получает интерфейс IDropTarget для элемента управления ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Элементы управления Windows для TB_GETOBJECT сообщений
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136815"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="03783-104">\_Сообщение об ОБЪЕКТЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="03783-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="03783-105">Получает [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="03783-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="03783-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03783-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03783-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03783-108">Идентификатор запрашиваемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="03783-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="03783-109">Это значение должно указывать на **IID \_ интерфейс IDropTarget**.</span><span class="sxs-lookup"><span data-stu-id="03783-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="03783-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03783-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03783-111">Адрес, получающий указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="03783-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="03783-112">При возникновении ошибки в этот адрес помещается **пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="03783-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03783-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03783-113">Return value</span></span>

<span data-ttu-id="03783-114">Возвращает значение **HRESULT** , указывающее на успешное выполнение или сбой операции.</span><span class="sxs-lookup"><span data-stu-id="03783-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="03783-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03783-115">Remarks</span></span>

<span data-ttu-id="03783-116">Панель инструментов [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) используется панелью инструментов, когда объекты перетаскиваются на него или отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="03783-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="03783-117">Требования</span><span class="sxs-lookup"><span data-stu-id="03783-117">Requirements</span></span>



| <span data-ttu-id="03783-118">Требование</span><span class="sxs-lookup"><span data-stu-id="03783-118">Requirement</span></span> | <span data-ttu-id="03783-119">Значение</span><span class="sxs-lookup"><span data-stu-id="03783-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03783-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03783-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03783-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03783-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03783-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03783-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03783-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03783-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03783-124">Header</span><span class="sxs-lookup"><span data-stu-id="03783-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03783-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="03783-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


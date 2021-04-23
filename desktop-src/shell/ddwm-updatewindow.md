---
description: Указывает, что окно удаления изображения будет обновляться с использованием новых данных ДРОПДЕСКРИПТИОН.
title: Сообщение DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984316"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="e754e-103">\_Сообщение ддвм упдатевиндов</span><span class="sxs-lookup"><span data-stu-id="e754e-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="e754e-104">Указывает, что окно удаления изображения будет обновляться с использованием новых данных [**дропдескриптион**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .</span><span class="sxs-lookup"><span data-stu-id="e754e-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="e754e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e754e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e754e-106">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e754e-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e754e-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e754e-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e754e-108">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e754e-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e754e-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e754e-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e754e-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="e754e-110">Remarks</span></span>

<span data-ttu-id="e754e-111">ДДВМ \_ упдатевиндов определяется как WM \_ User + 3.</span><span class="sxs-lookup"><span data-stu-id="e754e-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="e754e-112">При изменении состояния операции удаления (например, в ответ на клавишу-модификатор)[**интерфейс IDropTarget::D раговер**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) возвращает новое значение [**Дропеффект**](../com/dropeffect-constants.md) (это **дропеффект** может также быть получено с помощью [**идропсаурце:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span><span class="sxs-lookup"><span data-stu-id="e754e-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="e754e-113">В ответ приложение обновляет структуру [**дропдескриптион**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) целевого объекта перетаскивания на новое значение [**дропимажетипе**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) , которое указывает на оформление, применяемое к визуальному элементу окна перетаскивания; Например, указывает, что файл копируется, а не перемещен, или что объект не может быть удален в это расположение.</span><span class="sxs-lookup"><span data-stu-id="e754e-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="e754e-114">Однако визуальные элементы не обновляются, пока объект не получит сообщение **ддвм \_ упдатевиндов** .</span><span class="sxs-lookup"><span data-stu-id="e754e-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="e754e-115">Формат буфера обмена [драгвиндов](clipboard.md) предоставляет **HWND** окна, перетащив получателя, в отправителя сообщения **ддвм \_ упдатевиндов** .</span><span class="sxs-lookup"><span data-stu-id="e754e-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e754e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e754e-116">Requirements</span></span>



| <span data-ttu-id="e754e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e754e-117">Requirement</span></span> | <span data-ttu-id="e754e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e754e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e754e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e754e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e754e-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e754e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e754e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e754e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e754e-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e754e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 

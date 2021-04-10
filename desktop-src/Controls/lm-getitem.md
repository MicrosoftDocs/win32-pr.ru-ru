---
title: Сообщение LM_GETITEM (Коммктрл. h)
description: Извлекает состояния и атрибуты элемента.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Элементы управления Windows для LM_GETITEM сообщений
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135154"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="96e3b-104">\_Сообщение о сообщении LM</span><span class="sxs-lookup"><span data-stu-id="96e3b-104">LM\_GETITEM message</span></span>

<span data-ttu-id="96e3b-105">Извлекает состояния и атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="96e3b-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="96e3b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e3b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96e3b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="96e3b-108">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="96e3b-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="96e3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96e3b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="96e3b-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-litem">литем</a> , которая должна быть заполнена сведениями об элементе.</span><span class="sxs-lookup"><span data-stu-id="96e3b-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e3b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96e3b-111">Return value</span></span>

<span data-ttu-id="96e3b-112">Возвращает **значение true** , если сообщение завершается с ошибкой при получении указанных значений и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="96e3b-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="96e3b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96e3b-113">Remarks</span></span>

<span data-ttu-id="96e3b-114">С сообщением **LM- \_ Item** можно получить доступ к ссылкам только через числовой индекс, возвращенный в **iLink** члене [**литем**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="96e3b-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="96e3b-115">Обращение по ссылке через имя идентификатора, возвращенное в **сзид** , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="96e3b-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="96e3b-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="96e3b-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="96e3b-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="96e3b-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96e3b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="96e3b-118">Requirements</span></span>



| <span data-ttu-id="96e3b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="96e3b-119">Requirement</span></span> | <span data-ttu-id="96e3b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="96e3b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96e3b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96e3b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96e3b-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96e3b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96e3b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96e3b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96e3b-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96e3b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96e3b-125">Header</span><span class="sxs-lookup"><span data-stu-id="96e3b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e3b-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e3b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






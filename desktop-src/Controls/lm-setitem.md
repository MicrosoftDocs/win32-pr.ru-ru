---
title: Сообщение LM_SETITEM (Коммктрл. h)
description: Задает состояния и атрибуты элемента.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Элементы управления Windows для LM_SETITEM сообщений
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135150"
---
# <a name="lm_setitem-message"></a><span data-ttu-id="343ad-104">\_Сообщение СЕТИТЕМ LM</span><span class="sxs-lookup"><span data-stu-id="343ad-104">LM\_SETITEM message</span></span>

<span data-ttu-id="343ad-105">Задает состояния и атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="343ad-105">Sets the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="343ad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="343ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="343ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="343ad-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="343ad-108">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="343ad-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="343ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="343ad-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="343ad-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-litem">литем</a> , содержащую новые состояния и атрибуты, необходимые для ссылки.</span><span class="sxs-lookup"><span data-stu-id="343ad-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure containing the new states and attributes desired for the link.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="343ad-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="343ad-111">Return value</span></span>

<span data-ttu-id="343ad-112">Возвращает **значение true** , если сообщение завершается с ошибкой при установке указанных значений и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="343ad-112">Returns **TRUE** if the message succeeds in setting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="343ad-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="343ad-113">Remarks</span></span>

<span data-ttu-id="343ad-114">С сообщением [**LM- \_ Item**](lm-getitem.md) можно получить доступ к ссылкам только через числовой индекс, возвращенный в **iLink** члене [**литем**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="343ad-114">With the [**LM\_GETITEM**](lm-getitem.md) message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="343ad-115">Обращение по ссылке через имя идентификатора, возвращенное в **сзид** , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="343ad-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="343ad-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comctl32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="343ad-116">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="343ad-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="343ad-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="343ad-118">Требования</span><span class="sxs-lookup"><span data-stu-id="343ad-118">Requirements</span></span>



| <span data-ttu-id="343ad-119">Требование</span><span class="sxs-lookup"><span data-stu-id="343ad-119">Requirement</span></span> | <span data-ttu-id="343ad-120">Значение</span><span class="sxs-lookup"><span data-stu-id="343ad-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="343ad-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="343ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="343ad-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="343ad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="343ad-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="343ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="343ad-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="343ad-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="343ad-125">Header</span><span class="sxs-lookup"><span data-stu-id="343ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="343ad-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="343ad-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






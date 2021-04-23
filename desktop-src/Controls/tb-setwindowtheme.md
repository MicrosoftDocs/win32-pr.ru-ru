---
title: Сообщение TB_SETWINDOWTHEME (Коммктрл. h)
description: Задает визуальный стиль элемента управления ToolBar.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- Элементы управления Windows для TB_SETWINDOWTHEME сообщений
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137834"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="5011b-104">\_Сообщение SETWINDOWTHEME ТБ</span><span class="sxs-lookup"><span data-stu-id="5011b-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="5011b-105">Задает визуальный стиль элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="5011b-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5011b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5011b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5011b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5011b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5011b-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5011b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5011b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5011b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5011b-110">Указатель на строку в Юникоде, содержащую стиль отображения панели инструментов, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="5011b-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5011b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5011b-111">Return value</span></span>

<span data-ttu-id="5011b-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="5011b-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5011b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5011b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5011b-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="5011b-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5011b-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5011b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="5011b-116">Отправка этого сообщения эквивалентна вызову [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) на панели инструментов и ее элементе управления ToolTip, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="5011b-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="5011b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5011b-117">Requirements</span></span>



| <span data-ttu-id="5011b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5011b-118">Requirement</span></span> | <span data-ttu-id="5011b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5011b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5011b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5011b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5011b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5011b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5011b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5011b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5011b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5011b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5011b-124">Header</span><span class="sxs-lookup"><span data-stu-id="5011b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5011b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5011b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






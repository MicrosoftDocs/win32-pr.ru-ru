---
title: Сообщение EM_SETTOUCHOPTIONS (RichEdit. h)
description: Задает параметры касания, связанные с элементом управления Rich Edit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Элементы управления Windows для EM_SETTOUCHOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491199"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="7c94f-104">\_Сообщение СЕТТАУЧОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="7c94f-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="7c94f-105">Задает параметры касания, связанные с элементом управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="7c94f-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c94f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c94f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c94f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c94f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c94f-108">Параметр касания, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="7c94f-108">The touch option to set.</span></span> <span data-ttu-id="7c94f-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="7c94f-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7c94f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7c94f-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="7c94f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7c94f-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="7c94f-112"><dt>**RTO \_ шовхандлес**</dt></span><span class="sxs-lookup"><span data-stu-id="7c94f-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="7c94f-113">Отображение или скрытие дескрипторов захвата касания в зависимости от значения *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7c94f-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="7c94f-114"><dt>**RTO \_ дисаблехандлес**</dt></span><span class="sxs-lookup"><span data-stu-id="7c94f-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="7c94f-115">Включает или отключает обработку маркеров сенсорного захвата в зависимости от значения *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7c94f-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="7c94f-116">Если дескрипторы отключены, они скрываются, если они видимы и остаются скрытыми до тех пор, пока не изменится состояние сообщения **\_ сеттаучоптионс EM** .</span><span class="sxs-lookup"><span data-stu-id="7c94f-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="7c94f-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c94f-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c94f-118">Задайте значение **true** , чтобы показать или включить маркеры выбора касания, или **false** , чтобы скрыть или отключить маркеры сенсорного выбора.</span><span class="sxs-lookup"><span data-stu-id="7c94f-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c94f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c94f-119">Return value</span></span>

<span data-ttu-id="7c94f-120">Это сообщение возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7c94f-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c94f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7c94f-121">Requirements</span></span>



| <span data-ttu-id="7c94f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7c94f-122">Requirement</span></span> | <span data-ttu-id="7c94f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7c94f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c94f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c94f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c94f-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c94f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7c94f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c94f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c94f-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c94f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c94f-128">Header</span><span class="sxs-lookup"><span data-stu-id="7c94f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c94f-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c94f-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c94f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c94f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c94f-131">**EM \_ жеттаучоптионс**</span><span class="sxs-lookup"><span data-stu-id="7c94f-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 






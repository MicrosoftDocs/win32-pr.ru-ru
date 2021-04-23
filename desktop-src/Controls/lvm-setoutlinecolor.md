---
title: Сообщение LVM_SETOUTLINECOLOR (Коммктрл. h)
description: Задает цвет границы элемента управления "представление списка", если \_ \_ установлен расширенный стиль окна LVS ex бордерселект.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Элементы управления Windows для LVM_SETOUTLINECOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891442"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="1d001-104">\_Сообщение LVM сетаутлинеколор</span><span class="sxs-lookup"><span data-stu-id="1d001-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="1d001-105">Задает цвет границы элемента управления "представление списка", если установлен расширенный стиль окна [**LVS \_ ex \_ бордерселект**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1d001-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d001-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d001-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d001-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d001-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1d001-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1d001-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1d001-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d001-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1d001-110">Структура **COLORREF** , указывающая цвет для задания границы.</span><span class="sxs-lookup"><span data-stu-id="1d001-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d001-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d001-111">Return value</span></span>

<span data-ttu-id="1d001-112">Возвращает структуру **COLORREF** , содержащую цвет контура.</span><span class="sxs-lookup"><span data-stu-id="1d001-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d001-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d001-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d001-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="1d001-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1d001-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d001-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d001-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1d001-116">Requirements</span></span>



| <span data-ttu-id="1d001-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1d001-117">Requirement</span></span> | <span data-ttu-id="1d001-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1d001-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d001-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d001-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d001-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d001-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d001-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d001-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d001-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d001-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d001-123">Header</span><span class="sxs-lookup"><span data-stu-id="1d001-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d001-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d001-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






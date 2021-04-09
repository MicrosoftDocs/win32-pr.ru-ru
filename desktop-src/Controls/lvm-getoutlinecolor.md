---
title: Сообщение LVM_GETOUTLINECOLOR (Коммктрл. h)
description: Получает цвет границы элемента управления "представление списка", если \_ \_ установлен расширенный стиль окна LVS ex бордерселект.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Элементы управления Windows для LVM_GETOUTLINECOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892446"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="1a40c-104">\_Сообщение LVM жетаутлинеколор</span><span class="sxs-lookup"><span data-stu-id="1a40c-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="1a40c-105">Получает цвет границы элемента управления "представление списка", если установлен расширенный стиль окна [**LVS \_ ex \_ бордерселект**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1a40c-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a40c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a40c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a40c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a40c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1a40c-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1a40c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1a40c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a40c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1a40c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1a40c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a40c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a40c-111">Return value</span></span>

<span data-ttu-id="1a40c-112">Возвращает структуру **COLORREF** , содержащую цвет границы элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="1a40c-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a40c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a40c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a40c-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="1a40c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1a40c-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a40c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a40c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1a40c-116">Requirements</span></span>



| <span data-ttu-id="1a40c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1a40c-117">Requirement</span></span> | <span data-ttu-id="1a40c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1a40c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a40c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a40c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1a40c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a40c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a40c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a40c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1a40c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a40c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a40c-123">Header</span><span class="sxs-lookup"><span data-stu-id="1a40c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a40c-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a40c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






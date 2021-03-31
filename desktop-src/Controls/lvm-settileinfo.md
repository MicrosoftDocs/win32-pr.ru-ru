---
title: Сообщение LVM_SETTILEINFO (Коммктрл. h)
description: Задает сведения для существующей плитки элемента управления "представление списка".
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Элементы управления Windows для LVM_SETTILEINFO сообщений
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135587"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="937dc-104">\_Сообщение LVM сеттилеинфо</span><span class="sxs-lookup"><span data-stu-id="937dc-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="937dc-105">Задает сведения для существующей плитки элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="937dc-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="937dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="937dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="937dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="937dc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="937dc-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="937dc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="937dc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="937dc-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="937dc-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**лвтилеинфо**</a> , содержащую сведения, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="937dc-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="937dc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="937dc-111">Return value</span></span>

<span data-ttu-id="937dc-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="937dc-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="937dc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="937dc-113">Remarks</span></span>

<span data-ttu-id="937dc-114">**LVM \_ СЕТТИЛЕИНФО** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="937dc-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="937dc-115">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="937dc-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="937dc-116">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="937dc-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="937dc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="937dc-117">Requirements</span></span>



| <span data-ttu-id="937dc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="937dc-118">Requirement</span></span> | <span data-ttu-id="937dc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="937dc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="937dc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="937dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="937dc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="937dc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="937dc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="937dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="937dc-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="937dc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="937dc-124">Header</span><span class="sxs-lookup"><span data-stu-id="937dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="937dc-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="937dc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






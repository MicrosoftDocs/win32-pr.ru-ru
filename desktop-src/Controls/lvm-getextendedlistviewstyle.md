---
title: Сообщение LVM_GETEXTENDEDLISTVIEWSTYLE (Коммктрл. h)
description: Возвращает расширенные стили, используемые в данный момент для данного элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетекстендедлиствиевстиле ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Элементы управления Windows для LVM_GETEXTENDEDLISTVIEWSTYLE сообщений
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071119"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="7f78b-105">\_Сообщение LVM жетекстендедлиствиевстиле</span><span class="sxs-lookup"><span data-stu-id="7f78b-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="7f78b-106">Возвращает расширенные стили, используемые в данный момент для данного элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="7f78b-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="7f78b-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетекстендедлиствиевстиле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .</span><span class="sxs-lookup"><span data-stu-id="7f78b-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f78b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f78b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f78b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f78b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7f78b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7f78b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7f78b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f78b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7f78b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7f78b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f78b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f78b-113">Return value</span></span>

<span data-ttu-id="7f78b-114">Возвращает **DWORD** , представляющий стили, используемые в данный момент для данного элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="7f78b-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="7f78b-115">Это значение может быть сочетанием [расширенных стилей List-View](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="7f78b-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f78b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7f78b-116">Requirements</span></span>



| <span data-ttu-id="7f78b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7f78b-117">Requirement</span></span> | <span data-ttu-id="7f78b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7f78b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f78b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f78b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f78b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f78b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f78b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f78b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f78b-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f78b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f78b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7f78b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f78b-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f78b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






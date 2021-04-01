---
title: Сообщение LVM_GETGROUPINFO (Коммктрл. h)
description: Возвращает сведения о группе.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Элементы управления Windows для LVM_GETGROUPINFO сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071457"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="2de9f-104">\_Сообщение LVM жетграупинфо</span><span class="sxs-lookup"><span data-stu-id="2de9f-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="2de9f-105">Возвращает сведения о группе.</span><span class="sxs-lookup"><span data-stu-id="2de9f-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="2de9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2de9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2de9f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2de9f-108">Идентификатор, указывающий группу, сведения о которой извлекаются.</span><span class="sxs-lookup"><span data-stu-id="2de9f-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="2de9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2de9f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2de9f-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**лвграуп**</a> , которая получает извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="2de9f-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="2de9f-111">Задайте для элемента **кбсизе** этой структуры значение sizeof (лвграуп).</span><span class="sxs-lookup"><span data-stu-id="2de9f-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de9f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2de9f-112">Return value</span></span>

<span data-ttu-id="2de9f-113">Возвращает идентификатор группы в случае успеха или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2de9f-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de9f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2de9f-114">Remarks</span></span>

<span data-ttu-id="2de9f-115">Прежде чем пытаться получить заголовок для группы, сначала убедитесь, что у группы нет \_ стиля лбгс.</span><span class="sxs-lookup"><span data-stu-id="2de9f-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="2de9f-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="2de9f-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2de9f-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2de9f-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2de9f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2de9f-118">Requirements</span></span>



| <span data-ttu-id="2de9f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2de9f-119">Requirement</span></span> | <span data-ttu-id="2de9f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2de9f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2de9f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2de9f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2de9f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2de9f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2de9f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2de9f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2de9f-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2de9f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2de9f-125">Header</span><span class="sxs-lookup"><span data-stu-id="2de9f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2de9f-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de9f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






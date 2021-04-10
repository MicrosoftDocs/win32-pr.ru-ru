---
title: Сообщение LVM_SETGROUPINFO (Коммктрл. h)
description: Задает сведения о группе.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Элементы управления Windows для LVM_SETGROUPINFO сообщений
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071114"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="c995b-104">\_Сообщение LVM сетграупинфо</span><span class="sxs-lookup"><span data-stu-id="c995b-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="c995b-105">Задает сведения о группе.</span><span class="sxs-lookup"><span data-stu-id="c995b-105">Sets group information.</span></span> <span data-ttu-id="c995b-106">Отправьте это сообщение явным образом или с помощью макроса [**\_ сетграупинфо ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .</span><span class="sxs-lookup"><span data-stu-id="c995b-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c995b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c995b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c995b-108">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c995b-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="c995b-109">Идентификатор, указывающий группу, сведения о которой необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="c995b-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="c995b-110">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c995b-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="c995b-111">Указатель на структуру [**лвграуп**](windows/win32/api/commctrl/ns-commctrl-lvgroup) , содержащую сведения, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="c995b-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c995b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c995b-112">Return value</span></span>

<span data-ttu-id="c995b-113">Возвращает идентификатор группы в случае успеха или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c995b-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c995b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c995b-114">Remarks</span></span>

<span data-ttu-id="c995b-115">Чтобы изменить идентификатор группы для существующей группы, добавьте <b>LVGF_GROUPID</b> в <b>лвграуп. Mask</b> и задайте <b>лвграуп. играупид</b> в качестве нового идентификатора.</span><span class="sxs-lookup"><span data-stu-id="c995b-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="c995b-116">Вызов завершится ошибкой, если <b>лвграуп. играупид</b> содержит идентификатор существующей группы.</span><span class="sxs-lookup"><span data-stu-id="c995b-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="c995b-117">Обновление других свойств существующей группы (например, обновление выравнивания текста верхнего или нижнего колонтитула для группы, <b>уалигн</b>) <b>лвграуп. Mask</b> не должна содержать <b>LVGF_GROUPID</b>, иначе обновление завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c995b-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="c995b-118">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c995b-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c995b-119">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c995b-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c995b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c995b-120">Requirements</span></span>



| <span data-ttu-id="c995b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c995b-121">Requirement</span></span> | <span data-ttu-id="c995b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c995b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c995b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c995b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c995b-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c995b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c995b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c995b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c995b-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c995b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c995b-127">Header</span><span class="sxs-lookup"><span data-stu-id="c995b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c995b-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c995b-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






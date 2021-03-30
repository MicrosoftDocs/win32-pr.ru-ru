---
title: Сообщение LVM_GETGROUPINFOBYINDEX (Коммктрл. h)
description: Возвращает сведения о указанной группе. Отправьте это сообщение явным образом или с помощью \_ макроса Жетграупинфобиндекс ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Элементы управления Windows для LVM_GETGROUPINFOBYINDEX сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136418"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="ab61a-105">\_Сообщение LVM жетграупинфобиндекс</span><span class="sxs-lookup"><span data-stu-id="ab61a-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="ab61a-106">Возвращает сведения о указанной группе.</span><span class="sxs-lookup"><span data-stu-id="ab61a-106">Gets information on a specified group.</span></span> <span data-ttu-id="ab61a-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетграупинфобиндекс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .</span><span class="sxs-lookup"><span data-stu-id="ab61a-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab61a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab61a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab61a-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab61a-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab61a-110">Индекс группы.</span><span class="sxs-lookup"><span data-stu-id="ab61a-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="ab61a-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ab61a-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab61a-112">Указатель на структуру [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) для получения сведений о группе, заданной параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ab61a-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="ab61a-113">Вызывающий процесс отвечает за выделение памяти для структуры и всех буферов в структуре, например, на которую указывает элемент **псзеадер** .</span><span class="sxs-lookup"><span data-stu-id="ab61a-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="ab61a-114">Задайте все элементы, которые являются производными структуры, например **кчхеадер** размер буфера, на который указывает **псзеадер** в **Вчарс** , включая завершающее **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ab61a-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="ab61a-115">Задайте для **кбсизе** значение sizeof (лвграуп).</span><span class="sxs-lookup"><span data-stu-id="ab61a-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="ab61a-116">Получатель сообщений отвечает за присвоение членам структуры сведений о группе, заданной параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ab61a-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab61a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab61a-117">Return value</span></span>

<span data-ttu-id="ab61a-118">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ab61a-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab61a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ab61a-119">Requirements</span></span>



| <span data-ttu-id="ab61a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ab61a-120">Requirement</span></span> | <span data-ttu-id="ab61a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ab61a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab61a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab61a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ab61a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab61a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab61a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab61a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ab61a-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab61a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab61a-126">Header</span><span class="sxs-lookup"><span data-stu-id="ab61a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab61a-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab61a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






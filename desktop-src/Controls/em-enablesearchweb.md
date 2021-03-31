---
title: Сообщение EM_ENABLESEARCHWEB (Коммктрл. h)
description: Включает или отключает функцию "Поиск в Интернете" и запись в контекстном меню.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Элементы управления Windows для EM_ENABLESEARCHWEB сообщений
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988913"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="e5931-104">\_Сообщение ЕНАБЛЕСЕАРЧВЕБ EM</span><span class="sxs-lookup"><span data-stu-id="e5931-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="e5931-105">Включает или отключает функцию "Поиск в Интернете" и запись в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="e5931-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5931-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5931-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5931-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5931-108">Значение **true** указывает, что функция "Поиск в Интернете" включена, а значение " **ложь** " означает, что она отключена.</span><span class="sxs-lookup"><span data-stu-id="e5931-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e5931-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5931-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5931-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e5931-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5931-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5931-111">Return value</span></span>

<span data-ttu-id="e5931-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e5931-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5931-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5931-113">Remarks</span></span>

<span data-ttu-id="e5931-114">Если отключить "Поиск в Интернете" с помощью этого сообщения, сообщение [**EM \_ сеарчвеб**](em-searchweb.md) не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="e5931-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5931-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e5931-115">Requirements</span></span>



| <span data-ttu-id="e5931-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e5931-116">Requirement</span></span> | <span data-ttu-id="e5931-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e5931-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5931-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5931-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5931-119">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="e5931-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5931-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5931-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5931-121">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="e5931-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5931-122">Header</span><span class="sxs-lookup"><span data-stu-id="e5931-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5931-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5931-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5931-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5931-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5931-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e5931-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5931-126">**EM \_ сеарчвеб**</span><span class="sxs-lookup"><span data-stu-id="e5931-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 






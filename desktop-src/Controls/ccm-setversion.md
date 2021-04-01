---
title: Сообщение CCM_SETVERSION (Коммктрл. h)
description: Это сообщение используется для информирования элемента управления о том, что ожидается поведение, связанное с определенной версией.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Элементы управления Windows для CCM_SETVERSION сообщений
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071786"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="4bde7-104">\_Сообщение СЕТВЕРСИОН CCM</span><span class="sxs-lookup"><span data-stu-id="4bde7-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="4bde7-105">Это сообщение используется для информирования элемента управления о том, что ожидается поведение, связанное с определенной версией.</span><span class="sxs-lookup"><span data-stu-id="4bde7-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bde7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bde7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bde7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bde7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bde7-108">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="4bde7-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="4bde7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bde7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4bde7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4bde7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bde7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bde7-111">Return value</span></span>

<span data-ttu-id="4bde7-112">Возвращает версию, указанную в предыдущем сообщении **CCM \_ сетверсион** .</span><span class="sxs-lookup"><span data-stu-id="4bde7-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="4bde7-113">Если параметру *wParam* задано значение, большее, чем текущая версия DLL, возвращается-1.</span><span class="sxs-lookup"><span data-stu-id="4bde7-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bde7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bde7-114">Remarks</span></span>

<span data-ttu-id="4bde7-115">В некоторых случаях элемент управления может вести себя по-разному в зависимости от версии.</span><span class="sxs-lookup"><span data-stu-id="4bde7-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="4bde7-116">В основном это относится к ошибкам, исправленным в более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="4bde7-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="4bde7-117">Сообщение **CCM \_ сетверсион** позволяет информировать элемент управления о ожидаемом поведении.</span><span class="sxs-lookup"><span data-stu-id="4bde7-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="4bde7-118">Вы можете определить, какую версию вы указали, отправив сообщение [**CCM- \_ версии**](ccm-getversion.md) .</span><span class="sxs-lookup"><span data-stu-id="4bde7-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="4bde7-119">Пример использования этого сообщения см. в разделе [пользовательский вывод с помощью List-View и Tree-View элементов управления](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="4bde7-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="4bde7-120">Если установлена версия ComCtl32.dll 6, независимо от значения, заданного в параметре *wParam*, сообщение **CCM \_ сетверсион** Возвращает версию 6.</span><span class="sxs-lookup"><span data-stu-id="4bde7-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="4bde7-121">Это сообщение задает только номер версии для элемента управления, в который он отправляется.</span><span class="sxs-lookup"><span data-stu-id="4bde7-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4bde7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4bde7-122">Requirements</span></span>



| <span data-ttu-id="4bde7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4bde7-123">Requirement</span></span> | <span data-ttu-id="4bde7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4bde7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bde7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bde7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4bde7-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4bde7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4bde7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bde7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4bde7-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4bde7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4bde7-129">Header</span><span class="sxs-lookup"><span data-stu-id="4bde7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bde7-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bde7-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Сообщение LM_HITTEST (Коммктрл. h)
description: Определяет, щелкнул ли пользователь указанную ссылку.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Элементы управления Windows для LM_HITTEST сообщений
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891453"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="2500a-104">\_Сообщение HITTEST LM</span><span class="sxs-lookup"><span data-stu-id="2500a-104">LM\_HITTEST message</span></span>

<span data-ttu-id="2500a-105">Определяет, щелкнул ли пользователь указанную ссылку.</span><span class="sxs-lookup"><span data-stu-id="2500a-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="2500a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2500a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2500a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2500a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2500a-108">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2500a-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="2500a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2500a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2500a-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**лхиттестинфо**</a> для заполнения данными о ссылке, которую щелкнул пользователь, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="2500a-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2500a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2500a-111">Return value</span></span>

<span data-ttu-id="2500a-112">Возвращает **значение true** , если пользователь щелкнул ссылку; в противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2500a-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2500a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2500a-113">Remarks</span></span>

<span data-ttu-id="2500a-114">Если сообщение **\_ HITTEST LM** выполняется, система заполняет [**Литем. ILink**](/windows/win32/api/commctrl/ns-commctrl-litem) и **литем. сзид**.</span><span class="sxs-lookup"><span data-stu-id="2500a-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="2500a-115">Если сообщение **\_ HITTEST LM** не выполняется, не считайте, что любая информация в **литем** является допустимой.</span><span class="sxs-lookup"><span data-stu-id="2500a-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="2500a-116">Чтобы использовать этот API, необходимо предоставить манифест, задающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="2500a-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2500a-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2500a-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2500a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2500a-118">Requirements</span></span>



| <span data-ttu-id="2500a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2500a-119">Requirement</span></span> | <span data-ttu-id="2500a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2500a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2500a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2500a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2500a-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2500a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2500a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2500a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2500a-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2500a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2500a-125">Header</span><span class="sxs-lookup"><span data-stu-id="2500a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2500a-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2500a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






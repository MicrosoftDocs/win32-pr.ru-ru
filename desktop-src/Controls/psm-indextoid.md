---
title: Сообщение PSM_INDEXTOID (Пршт. h)
description: Принимает индекс страницы свойств и возвращает идентификатор ресурса. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстоид.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Элементы управления Windows для PSM_INDEXTOID сообщений
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071777"
---
# <a name="psm_indextoid-message"></a><span data-ttu-id="3d015-105">\_Сообщение ПСМ индекстоид</span><span class="sxs-lookup"><span data-stu-id="3d015-105">PSM\_INDEXTOID message</span></span>

<span data-ttu-id="3d015-106">Принимает индекс страницы свойств и возвращает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d015-106">Takes the index of a property sheet page and returns its resource ID.</span></span> <span data-ttu-id="3d015-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстоид**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .</span><span class="sxs-lookup"><span data-stu-id="3d015-107">You can send this message explicitly or use the [**PropSheet\_IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d015-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d015-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d015-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d015-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d015-110">Отсчитываемый от нуля индекс страницы.</span><span class="sxs-lookup"><span data-stu-id="3d015-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="3d015-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d015-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d015-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3d015-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d015-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d015-113">Return value</span></span>

<span data-ttu-id="3d015-114">Возвращает идентификатор ресурса страницы свойств, указанной параметром *wParam* в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="3d015-114">Returns the resource ID of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="3d015-115">В противном случае возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="3d015-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d015-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3d015-116">Requirements</span></span>



| <span data-ttu-id="3d015-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3d015-117">Requirement</span></span> | <span data-ttu-id="3d015-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3d015-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d015-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d015-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d015-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d015-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d015-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d015-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d015-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d015-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d015-123">Header</span><span class="sxs-lookup"><span data-stu-id="3d015-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d015-124"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d015-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






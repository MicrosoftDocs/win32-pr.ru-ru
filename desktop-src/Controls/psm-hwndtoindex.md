---
title: Сообщение PSM_HWNDTOINDEX (Пршт. h)
description: Принимает маркер окна страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ хвндтоиндекс.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Элементы управления Windows для PSM_HWNDTOINDEX сообщений
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136243"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="cb0c2-105">\_Сообщение ПСМ хвндтоиндекс</span><span class="sxs-lookup"><span data-stu-id="cb0c2-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="cb0c2-106">Принимает маркер окна страницы свойств и возвращает индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="cb0c2-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="cb0c2-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ хвндтоиндекс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .</span><span class="sxs-lookup"><span data-stu-id="cb0c2-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb0c2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb0c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb0c2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb0c2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb0c2-110">Обработчик для окна страницы.</span><span class="sxs-lookup"><span data-stu-id="cb0c2-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="cb0c2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb0c2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb0c2-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cb0c2-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb0c2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb0c2-113">Return value</span></span>

<span data-ttu-id="cb0c2-114">Возвращает отсчитываемый от нуля индекс страницы вкладки свойств, указанной параметром *wParam* в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="cb0c2-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="cb0c2-115">Иначе возвращается значение -1.</span><span class="sxs-lookup"><span data-stu-id="cb0c2-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb0c2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cb0c2-116">Requirements</span></span>



| <span data-ttu-id="cb0c2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cb0c2-117">Requirement</span></span> | <span data-ttu-id="cb0c2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cb0c2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0c2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb0c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb0c2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb0c2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb0c2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb0c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb0c2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb0c2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cb0c2-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb0c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb0c2-124"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb0c2-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






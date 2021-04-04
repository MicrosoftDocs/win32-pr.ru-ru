---
title: Сообщение PSM_IDTOINDEX (Пршт. h)
description: Принимает идентификатор ресурса страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ идтоиндекс.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Элементы управления Windows для PSM_IDTOINDEX сообщений
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136962"
---
# <a name="psm_idtoindex-message"></a><span data-ttu-id="ef7ae-105">\_Сообщение ПСМ идтоиндекс</span><span class="sxs-lookup"><span data-stu-id="ef7ae-105">PSM\_IDTOINDEX message</span></span>

<span data-ttu-id="ef7ae-106">Принимает идентификатор ресурса страницы свойств и возвращает индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-106">Takes the resource ID of a property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="ef7ae-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ идтоиндекс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .</span><span class="sxs-lookup"><span data-stu-id="ef7ae-107">You can send this message explicitly or use the [**PropSheet\_IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef7ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef7ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef7ae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef7ae-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef7ae-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ef7ae-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef7ae-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef7ae-112">Идентификатор ресурса страницы.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-112">Resource ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef7ae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef7ae-113">Return value</span></span>

<span data-ttu-id="ef7ae-114">Возвращает отсчитываемый от нуля индекс страницы вкладки свойств, указанной параметром *lParam* в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="ef7ae-115">Иначе возвращается значение -1.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef7ae-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ef7ae-116">Requirements</span></span>



| <span data-ttu-id="ef7ae-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ef7ae-117">Requirement</span></span> | <span data-ttu-id="ef7ae-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ef7ae-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7ae-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef7ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7ae-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef7ae-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ef7ae-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef7ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7ae-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef7ae-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef7ae-123">Header</span><span class="sxs-lookup"><span data-stu-id="ef7ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef7ae-124"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef7ae-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






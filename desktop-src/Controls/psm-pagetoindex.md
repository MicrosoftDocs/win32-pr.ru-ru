---
title: Сообщение PSM_PAGETOINDEX (Пршт. h)
description: Принимает маркер ХПРОПШИТПАЖЕ страницы свойств и возвращает индекс, начинающийся с нуля. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ пажетоиндекс.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Элементы управления Windows для PSM_PAGETOINDEX сообщений
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654542"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="e36bc-105">\_Сообщение ПСМ пажетоиндекс</span><span class="sxs-lookup"><span data-stu-id="e36bc-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="e36bc-106">Принимает маркер ХПРОПШИТПАЖЕ страницы свойств и возвращает индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="e36bc-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="e36bc-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ пажетоиндекс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .</span><span class="sxs-lookup"><span data-stu-id="e36bc-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e36bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e36bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e36bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e36bc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e36bc-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e36bc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e36bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e36bc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e36bc-112">ХПРОПШИТПАЖЕ маркер на страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="e36bc-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e36bc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e36bc-113">Return value</span></span>

<span data-ttu-id="e36bc-114">Возвращает отсчитываемый от нуля индекс страницы вкладки свойств, указанной параметром *lParam* в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="e36bc-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="e36bc-115">Иначе возвращается значение -1.</span><span class="sxs-lookup"><span data-stu-id="e36bc-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e36bc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e36bc-116">Requirements</span></span>



| <span data-ttu-id="e36bc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e36bc-117">Requirement</span></span> | <span data-ttu-id="e36bc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e36bc-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e36bc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e36bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e36bc-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e36bc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e36bc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e36bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e36bc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e36bc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e36bc-123">Header</span><span class="sxs-lookup"><span data-stu-id="e36bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e36bc-124"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="e36bc-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






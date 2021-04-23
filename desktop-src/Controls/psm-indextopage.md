---
title: Сообщение PSM_INDEXTOPAGE (Пршт. h)
description: Принимает индекс страницы свойств и возвращает его обработчик ХПРОПШИТПАЖЕ. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстопаже.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Элементы управления Windows для PSM_INDEXTOPAGE сообщений
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492132"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="96306-105">\_Сообщение ПСМ индекстопаже</span><span class="sxs-lookup"><span data-stu-id="96306-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="96306-106">Принимает индекс страницы свойств и возвращает его обработчик ХПРОПШИТПАЖЕ.</span><span class="sxs-lookup"><span data-stu-id="96306-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="96306-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстопаже**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .</span><span class="sxs-lookup"><span data-stu-id="96306-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="96306-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96306-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96306-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96306-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96306-110">Отсчитываемый от нуля индекс страницы.</span><span class="sxs-lookup"><span data-stu-id="96306-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="96306-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96306-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96306-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="96306-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96306-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96306-113">Return value</span></span>

<span data-ttu-id="96306-114">Возвращает маркер ХПРОПШИТПАЖЕ страницы свойств, указанный параметром *wParam* в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="96306-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="96306-115">В противном случае возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="96306-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="96306-116">Требования</span><span class="sxs-lookup"><span data-stu-id="96306-116">Requirements</span></span>



| <span data-ttu-id="96306-117">Требование</span><span class="sxs-lookup"><span data-stu-id="96306-117">Requirement</span></span> | <span data-ttu-id="96306-118">Значение</span><span class="sxs-lookup"><span data-stu-id="96306-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96306-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96306-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96306-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96306-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96306-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96306-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96306-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96306-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="96306-123">Header</span><span class="sxs-lookup"><span data-stu-id="96306-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96306-124"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="96306-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






---
title: Сообщение PSM_INDEXTOHWND (Пршт. h)
description: Принимает индекс страницы свойств и возвращает его маркер окна. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстохвнд.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Элементы управления Windows для PSM_INDEXTOHWND сообщений
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136954"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="a9c1d-105">\_Сообщение ПСМ индекстохвнд</span><span class="sxs-lookup"><span data-stu-id="a9c1d-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="a9c1d-106">Принимает индекс страницы свойств и возвращает его маркер окна.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="a9c1d-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстохвнд**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .</span><span class="sxs-lookup"><span data-stu-id="a9c1d-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9c1d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9c1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c1d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9c1d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c1d-110">Отсчитываемый от нуля индекс страницы.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="a9c1d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9c1d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c1d-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c1d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9c1d-113">Return value</span></span>

<span data-ttu-id="a9c1d-114">Возвращает маркер окна страницы свойств, заданного параметром *wParam* , если выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="a9c1d-115">В противном случае возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c1d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a9c1d-116">Requirements</span></span>



| <span data-ttu-id="a9c1d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a9c1d-117">Requirement</span></span> | <span data-ttu-id="a9c1d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a9c1d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c1d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9c1d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c1d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9c1d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9c1d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9c1d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c1d-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9c1d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a9c1d-123">Header</span><span class="sxs-lookup"><span data-stu-id="a9c1d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c1d-124"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c1d-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






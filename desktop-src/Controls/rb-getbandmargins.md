---
title: Сообщение RB_GETBANDMARGINS (Коммктрл. h)
description: Извлекает поля полосы.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- Элементы управления Windows для RB_GETBANDMARGINS сообщений
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988986"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="897fc-104">\_Сообщение ЖЕТБАНДМАРГИНС RB</span><span class="sxs-lookup"><span data-stu-id="897fc-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="897fc-105">Извлекает поля полосы.</span><span class="sxs-lookup"><span data-stu-id="897fc-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="897fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="897fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="897fc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="897fc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="897fc-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="897fc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="897fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="897fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="897fc-110">Указатель на структуру [**полей**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) , которая получает извлеченные поля.</span><span class="sxs-lookup"><span data-stu-id="897fc-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="897fc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="897fc-111">Return value</span></span>

<span data-ttu-id="897fc-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="897fc-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="897fc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="897fc-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="897fc-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="897fc-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="897fc-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="897fc-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="897fc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="897fc-116">Requirements</span></span>



| <span data-ttu-id="897fc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="897fc-117">Requirement</span></span> | <span data-ttu-id="897fc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="897fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="897fc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="897fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="897fc-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="897fc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="897fc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="897fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="897fc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="897fc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="897fc-123">Header</span><span class="sxs-lookup"><span data-stu-id="897fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="897fc-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="897fc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






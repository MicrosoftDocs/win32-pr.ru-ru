---
title: Сообщение EM_ISIME (RichEdit. h)
description: Определение с использованием текущего языкового стандарта ввода элемента управления редактирования является восточно-азиатским языковым стандартом.
ms.assetid: 606e9c7f-dd9e-44b3-b37d-d6838bc66818
keywords:
- Элементы управления Windows для EM_ISIME сообщений
topic_type:
- apiref
api_name:
- EM_ISIME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fe801fa8f5150aa342e431f62b971a959569304
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988266"
---
# <a name="em_isime-message"></a><span data-ttu-id="548a3-104">\_Сообщение ИСИМЕ EM</span><span class="sxs-lookup"><span data-stu-id="548a3-104">EM\_ISIME message</span></span>

<span data-ttu-id="548a3-105">Определение с использованием текущего языкового стандарта ввода элемента управления редактирования является восточно-азиатским языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="548a3-105">Determine with a rich edit control's current input locale is an East Asian locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="548a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="548a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="548a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="548a3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="548a3-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="548a3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="548a3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="548a3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="548a3-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="548a3-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="548a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="548a3-111">Return value</span></span>

<span data-ttu-id="548a3-112">Возвращает **значение true** , если это языковой стандарт Восточной Азии.</span><span class="sxs-lookup"><span data-stu-id="548a3-112">Returns **TRUE** if it is an East Asian locale.</span></span> <span data-ttu-id="548a3-113">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="548a3-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="548a3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="548a3-114">Requirements</span></span>



| <span data-ttu-id="548a3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="548a3-115">Requirement</span></span> | <span data-ttu-id="548a3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="548a3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="548a3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="548a3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="548a3-118">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="548a3-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="548a3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="548a3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="548a3-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="548a3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="548a3-121">Header</span><span class="sxs-lookup"><span data-stu-id="548a3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="548a3-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="548a3-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 






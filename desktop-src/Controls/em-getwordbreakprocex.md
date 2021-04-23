---
title: Сообщение EM_GETWORDBREAKPROCEX (RichEdit. h)
description: Извлекает адрес зарегистрированной в настоящий момент расширенной процедуры разбиения по словам для элемента управления расширенного редактирования.
ms.assetid: 391681b6-fba9-4fc8-8778-3b3bd45ee5d6
keywords:
- Элементы управления Windows для EM_GETWORDBREAKPROCEX сообщений
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890ef921a33dc387b17fddaa504bd15fa61ac505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892361"
---
# <a name="em_getwordbreakprocex-message"></a><span data-ttu-id="8cf29-104">\_Сообщение ЖЕТВОРДБРЕАКПРОЦЕКС EM</span><span class="sxs-lookup"><span data-stu-id="8cf29-104">EM\_GETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="8cf29-105">Извлекает адрес зарегистрированной в настоящий момент расширенной процедуры разбиения по словам для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="8cf29-105">Retrieves the address of the currently registered extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cf29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cf29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cf29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cf29-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8cf29-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8cf29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cf29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cf29-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8cf29-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf29-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cf29-111">Return value</span></span>

<span data-ttu-id="8cf29-112">Сообщение возвращает адрес текущей процедуры.</span><span class="sxs-lookup"><span data-stu-id="8cf29-112">The message returns the address of the current procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf29-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8cf29-113">Requirements</span></span>



| <span data-ttu-id="8cf29-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8cf29-114">Requirement</span></span> | <span data-ttu-id="8cf29-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf29-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf29-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cf29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf29-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cf29-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cf29-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cf29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf29-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cf29-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cf29-120">Header</span><span class="sxs-lookup"><span data-stu-id="8cf29-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf29-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf29-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 






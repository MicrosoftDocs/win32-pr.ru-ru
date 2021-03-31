---
title: Сообщение EM_SETPALETTE (RichEdit. h)
description: Изменяет палитру, которую элемент управления Rich Edit использует для окна его просмотра.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- Элементы управления Windows для EM_SETPALETTE сообщений
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071524"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="73fe7-104">\_Сообщение СЕТПАЛЕТТЕ EM</span><span class="sxs-lookup"><span data-stu-id="73fe7-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="73fe7-105">Изменяет палитру, которую элемент управления Rich Edit использует для окна его просмотра.</span><span class="sxs-lookup"><span data-stu-id="73fe7-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="73fe7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73fe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fe7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73fe7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73fe7-108">Обработчик для новой палитры, используемой элементом управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="73fe7-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="73fe7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73fe7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73fe7-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="73fe7-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fe7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73fe7-111">Return value</span></span>

<span data-ttu-id="73fe7-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="73fe7-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73fe7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73fe7-113">Remarks</span></span>

<span data-ttu-id="73fe7-114">Элемент управления Rich Edit не проверяет, является ли новая палитра допустимой.</span><span class="sxs-lookup"><span data-stu-id="73fe7-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="73fe7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="73fe7-115">Requirements</span></span>



| <span data-ttu-id="73fe7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="73fe7-116">Requirement</span></span> | <span data-ttu-id="73fe7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="73fe7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73fe7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73fe7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="73fe7-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73fe7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73fe7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73fe7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="73fe7-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73fe7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73fe7-122">Header</span><span class="sxs-lookup"><span data-stu-id="73fe7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="73fe7-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="73fe7-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 






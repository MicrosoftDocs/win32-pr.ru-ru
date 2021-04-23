---
title: Сообщение EM_EXLINEFROMCHAR (RichEdit. h)
description: Определяет, какая строка содержит указанный символ в элементе управления Rich Edit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- Элементы управления Windows для EM_EXLINEFROMCHAR сообщений
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493350"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="85d66-104">\_Сообщение ЕКСЛИНЕФРОМЧАР EM</span><span class="sxs-lookup"><span data-stu-id="85d66-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="85d66-105">Определяет, какая строка содержит указанный символ в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="85d66-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="85d66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d66-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85d66-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85d66-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="85d66-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="85d66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85d66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85d66-110">Отсчитываемый от нуля индекс символа.</span><span class="sxs-lookup"><span data-stu-id="85d66-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d66-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85d66-111">Return value</span></span>

<span data-ttu-id="85d66-112">Это сообщение возвращает отсчитываемый от нуля индекс строки.</span><span class="sxs-lookup"><span data-stu-id="85d66-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d66-113">Требования</span><span class="sxs-lookup"><span data-stu-id="85d66-113">Requirements</span></span>



| <span data-ttu-id="85d66-114">Требование</span><span class="sxs-lookup"><span data-stu-id="85d66-114">Requirement</span></span> | <span data-ttu-id="85d66-115">Значение</span><span class="sxs-lookup"><span data-stu-id="85d66-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85d66-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85d66-116">Minimum supported client</span></span><br/> | <span data-ttu-id="85d66-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85d66-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85d66-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85d66-118">Minimum supported server</span></span><br/> | <span data-ttu-id="85d66-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85d66-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85d66-120">Header</span><span class="sxs-lookup"><span data-stu-id="85d66-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="85d66-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="85d66-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 






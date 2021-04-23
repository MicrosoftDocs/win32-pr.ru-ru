---
title: Код уведомления EN_STARTCOMPOSITION (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что пользователь начал вводить текст с помощью IME или платформы текстовых служб.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137150"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="6d459-104">\_Код уведомления EN старткомпоситион</span><span class="sxs-lookup"><span data-stu-id="6d459-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="6d459-105">Сообщает родительскому окну элемента управления Rich Edit, что пользователь начал вводить текст с помощью IME или [платформы текстовых служб](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="6d459-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d459-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d459-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d459-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d459-108">Структура [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="6d459-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d459-109">Требования</span><span class="sxs-lookup"><span data-stu-id="6d459-109">Requirements</span></span>



| <span data-ttu-id="6d459-110">Требование</span><span class="sxs-lookup"><span data-stu-id="6d459-110">Requirement</span></span> | <span data-ttu-id="6d459-111">Значение</span><span class="sxs-lookup"><span data-stu-id="6d459-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d459-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d459-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6d459-113">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6d459-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6d459-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d459-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6d459-115">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6d459-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d459-116">Header</span><span class="sxs-lookup"><span data-stu-id="6d459-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d459-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d459-117"><dt>Richedit.h</dt></span></span> </dl> |



 


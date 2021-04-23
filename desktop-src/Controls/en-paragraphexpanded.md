---
title: Код уведомления EN_PARAGRAPHEXPANDED (RichEdit. h)
description: Сообщает родителю элемента управления Rich Edit, что структура была расширена. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- EN_PARAGRAPHEXPANDED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490872"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="1baf1-105">\_Код уведомления EN параграфекспандед</span><span class="sxs-lookup"><span data-stu-id="1baf1-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="1baf1-106">Сообщает родителю элемента управления Rich Edit, что структура была расширена.</span><span class="sxs-lookup"><span data-stu-id="1baf1-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="1baf1-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1baf1-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1baf1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1baf1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1baf1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1baf1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1baf1-110">Структура [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="1baf1-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1baf1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="1baf1-111">Requirements</span></span>



| <span data-ttu-id="1baf1-112">Требование</span><span class="sxs-lookup"><span data-stu-id="1baf1-112">Requirement</span></span> | <span data-ttu-id="1baf1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1baf1-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1baf1-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1baf1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1baf1-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1baf1-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1baf1-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1baf1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1baf1-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1baf1-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1baf1-118">Header</span><span class="sxs-lookup"><span data-stu-id="1baf1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1baf1-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1baf1-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 






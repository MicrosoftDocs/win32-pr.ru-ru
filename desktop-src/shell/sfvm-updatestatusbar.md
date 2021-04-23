---
description: 'Уведомляет объект обратного вызова о том, что строка состояния обновляется. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_UPDATESTATUSBAR (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997774"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="a681c-104">\_Сообщение сфвм упдатестатусбар</span><span class="sxs-lookup"><span data-stu-id="a681c-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="a681c-105">Уведомляет объект обратного вызова о том, что строка состояния обновляется.</span><span class="sxs-lookup"><span data-stu-id="a681c-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="a681c-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="a681c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="a681c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a681c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a681c-108">*финитиализе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a681c-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a681c-109">**Логическое** значение, которое устанавливается равным **true** , если строка состояния инициализируется.</span><span class="sxs-lookup"><span data-stu-id="a681c-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a681c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="a681c-110">Remarks</span></span>

<span data-ttu-id="a681c-111">При получении этого уведомления:</span><span class="sxs-lookup"><span data-stu-id="a681c-111">When you receive this notification:</span></span>

-   <span data-ttu-id="a681c-112">\_Если обновление будет обработано, возвращайте ОК.</span><span class="sxs-lookup"><span data-stu-id="a681c-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="a681c-113">Возвращает \_ значение HRESULT ( \_ УСПЕШНОе серьезность, 0, 1), чтобы объект представления системной папки установил текст строки состояния.</span><span class="sxs-lookup"><span data-stu-id="a681c-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="a681c-114">Возврат E \_ не удается, чтобы объект представления системной папки обрабатывал строку состояния.</span><span class="sxs-lookup"><span data-stu-id="a681c-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="a681c-115">Текст строки состояния по умолчанию выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a681c-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="a681c-116">Состояние</span><span class="sxs-lookup"><span data-stu-id="a681c-116">Status</span></span>                      | <span data-ttu-id="a681c-117">Текст строки состояния</span><span class="sxs-lookup"><span data-stu-id="a681c-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="a681c-118">Элементы не выбраны</span><span class="sxs-lookup"><span data-stu-id="a681c-118">No items selected</span></span>           | <span data-ttu-id="a681c-119">" \# \# Objects" (в папке)</span><span class="sxs-lookup"><span data-stu-id="a681c-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="a681c-120">Выбран один элемент</span><span class="sxs-lookup"><span data-stu-id="a681c-120">One item selected</span></span>           | <span data-ttu-id="a681c-121">Всплывающая подсказка для элемента, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="a681c-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="a681c-122">Выбрано более одного элемента</span><span class="sxs-lookup"><span data-stu-id="a681c-122">More than one item selected</span></span> | <span data-ttu-id="a681c-123">" \# \# объекты выбраны"</span><span class="sxs-lookup"><span data-stu-id="a681c-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="a681c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a681c-124">Requirements</span></span>



| <span data-ttu-id="a681c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a681c-125">Requirement</span></span> | <span data-ttu-id="a681c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a681c-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a681c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a681c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a681c-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a681c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a681c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a681c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a681c-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a681c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a681c-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a681c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a681c-132"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="a681c-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

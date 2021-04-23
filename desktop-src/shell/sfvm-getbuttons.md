---
description: 'Позволяет объекту обратного вызова указывать кнопки, добавляемые на панель инструментов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Сообщение SFVM_GETBUTTONS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911399"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="aeadf-104">Сообщение СФВМ с \_ кнопками</span><span class="sxs-lookup"><span data-stu-id="aeadf-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="aeadf-105">Позволяет объекту обратного вызова указывать кнопки, добавляемые на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="aeadf-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="aeadf-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="aeadf-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="aeadf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aeadf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeadf-108">*идкмдфирст \_ кбтнмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="aeadf-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeadf-109">Содержит 2 16-разрядные значения, Упакованные в параметр с помощью макроса [**макевпарам**](/windows/win32/api/winuser/nf-winuser-makewparam) .</span><span class="sxs-lookup"><span data-stu-id="aeadf-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="aeadf-110">Слово нижнего порядка содержит начальный идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="aeadf-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="aeadf-111">Слово высокого порядка содержит число добавляемых кнопок, как указано в предыдущем сообщении [**сфвм \_ жетбуттонинфо**](sfvm-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="aeadf-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="aeadf-112">*пбтн* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aeadf-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeadf-113">Адрес массива структур [**тббуттон**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , по одному для каждой кнопки, добавляемой на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="aeadf-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aeadf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="aeadf-114">Remarks</span></span>

<span data-ttu-id="aeadf-115">Этому сообщению предшествует сообщение [**сфвм \_ жетбуттонинфо**](sfvm-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="aeadf-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="aeadf-116">Объект обратного вызова должен обрабатывать это сообщение, чтобы указать количество кнопок и место их размещения на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="aeadf-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="aeadf-117">В зависимости от того, как объект обратного вызова реагирует на сообщение **сфвм \_ жетбуттонинфо** , кнопки, заданные параметром *пбтн* , добавляются или добавляются к стандартным кнопкам объекта представления системных папок или заменяют стандартный набор.</span><span class="sxs-lookup"><span data-stu-id="aeadf-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeadf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="aeadf-118">Requirements</span></span>



| <span data-ttu-id="aeadf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="aeadf-119">Requirement</span></span> | <span data-ttu-id="aeadf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="aeadf-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aeadf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aeadf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aeadf-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aeadf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aeadf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aeadf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aeadf-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aeadf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aeadf-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aeadf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeadf-126"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeadf-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

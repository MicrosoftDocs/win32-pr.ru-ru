---
description: 'Позволяет объекту обратного вызова указать, что анимация должна отображаться при перечислении элементов в фоновом потоке. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Сообщение SFVM_GETANIMATION (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156795"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="a6cff-104">\_Сообщение СФВМ анимации</span><span class="sxs-lookup"><span data-stu-id="a6cff-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="a6cff-105">Позволяет объекту обратного вызова указать, что анимация должна отображаться при перечислении элементов в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="a6cff-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="a6cff-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="a6cff-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="a6cff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6cff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6cff-108">*финст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a6cff-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cff-109">Описатель экземпляра модуля, из которого должен быть загружен ресурс.</span><span class="sxs-lookup"><span data-stu-id="a6cff-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="a6cff-110">*pwszName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a6cff-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cff-111">Указатель на строку в Юникоде, заканчивающуюся нулем, которая содержит путь к AVI-файлу или имя ресурса AVI.</span><span class="sxs-lookup"><span data-stu-id="a6cff-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="a6cff-112">Кроме того, этот параметр может состоять из идентификатора ресурса в младшем слове и 0 в слове высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="a6cff-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="a6cff-113">Чтобы создать это значение, используйте макрос [**макеинтресаурце**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="a6cff-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="a6cff-114">Элемент управления загружает ресурс из модуля, указанного параметром хинст.</span><span class="sxs-lookup"><span data-stu-id="a6cff-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="a6cff-115">Ресурс AVI должен иметь тип AVI.</span><span class="sxs-lookup"><span data-stu-id="a6cff-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6cff-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6cff-116">Remarks</span></span>

<span data-ttu-id="a6cff-117">По умолчанию объект представления системных папок отображает анимацию "фонарик" во время перечисления фона.</span><span class="sxs-lookup"><span data-stu-id="a6cff-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="a6cff-118">*финст* и *pwszName* будут переданы [элементу управления анимацией](../controls/animation-control-overview.md) с [**\_ открытым**](../controls/acm-open.md) сообщением ACM.</span><span class="sxs-lookup"><span data-stu-id="a6cff-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6cff-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a6cff-119">Requirements</span></span>



| <span data-ttu-id="a6cff-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a6cff-120">Requirement</span></span> | <span data-ttu-id="a6cff-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a6cff-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cff-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6cff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6cff-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6cff-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a6cff-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6cff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6cff-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6cff-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a6cff-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a6cff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6cff-127"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6cff-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

---
description: СФВМ \_ диддрагдроп может быть изменен или недоступен.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Сообщение SFVM_DIDDRAGDROP (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997826"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="8d911-103">\_Сообщение сфвм диддрагдроп</span><span class="sxs-lookup"><span data-stu-id="8d911-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="8d911-104">\[**Сфвм \_ ДИДДРАГДРОП** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8d911-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d911-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="8d911-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8d911-106">Уведомляет функцию обратного вызова о начале операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="8d911-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="8d911-107">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="8d911-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="8d911-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d911-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d911-109">*двеффект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d911-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d911-110">Описатель эффекты перетаскивания из перечисления [**дропеффект**](../com/dropeffect-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="8d911-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="8d911-111">Это достигается путем вызова [**шдодрагдроп**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span><span class="sxs-lookup"><span data-stu-id="8d911-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="8d911-112">*Пидо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d911-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d911-113">Указатель на экземпляр [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="8d911-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d911-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8d911-114">Requirements</span></span>



| <span data-ttu-id="8d911-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8d911-115">Requirement</span></span> | <span data-ttu-id="8d911-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8d911-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d911-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d911-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d911-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8d911-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8d911-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d911-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d911-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d911-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d911-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8d911-121">End of client support</span></span><br/>    | <span data-ttu-id="8d911-122">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="8d911-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="8d911-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8d911-123">End of server support</span></span><br/>    | <span data-ttu-id="8d911-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d911-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="8d911-125">Header</span><span class="sxs-lookup"><span data-stu-id="8d911-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d911-126"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d911-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

---
description: 'Уведомляет объект обратного вызова о том, что один из его панелей инструментов или команд меню был вызван пользователем. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Сообщение SFVM_INVOKECOMMAND (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913312"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="a275b-104">\_Сообщение сфвм инвокекомманд</span><span class="sxs-lookup"><span data-stu-id="a275b-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="a275b-105">Уведомляет объект обратного вызова о том, что один из его панелей инструментов или команд меню был вызван пользователем.</span><span class="sxs-lookup"><span data-stu-id="a275b-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="a275b-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="a275b-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="a275b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a275b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a275b-108">*идкмд* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a275b-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a275b-109">Идентификатор команды выбранной панели инструментов или пункта меню.</span><span class="sxs-lookup"><span data-stu-id="a275b-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a275b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="a275b-110">Remarks</span></span>

<span data-ttu-id="a275b-111">Это сообщение представляет собой ту же функцию, что [**и \_ командное сообщение WM**](../menurc/wm-command.md) в обычной процедуре окна.</span><span class="sxs-lookup"><span data-stu-id="a275b-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="a275b-112">Он позволяет объекту обратного вызова обменять любые элементы, добавленные в обозреватель Windows или строку меню.</span><span class="sxs-lookup"><span data-stu-id="a275b-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="a275b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a275b-113">Requirements</span></span>



| <span data-ttu-id="a275b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a275b-114">Requirement</span></span> | <span data-ttu-id="a275b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a275b-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a275b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a275b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a275b-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a275b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a275b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a275b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a275b-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a275b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a275b-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a275b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a275b-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="a275b-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

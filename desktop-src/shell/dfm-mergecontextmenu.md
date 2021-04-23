---
description: Разрешает обратный вызов для добавления элементов в меню.
title: Сообщение DFM_MERGECONTEXTMENU (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d469f9764b5e377e5f47227d3414f246441d3505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984297"
---
# <a name="dfm_mergecontextmenu-message"></a><span data-ttu-id="33539-103">\_Сообщение DFM мержеконтекстмену</span><span class="sxs-lookup"><span data-stu-id="33539-103">DFM\_MERGECONTEXTMENU message</span></span>

<span data-ttu-id="33539-104">Разрешает обратный вызов для добавления элементов в меню.</span><span class="sxs-lookup"><span data-stu-id="33539-104">Allows the callback to add items to the menu.</span></span>


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="33539-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="33539-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33539-106">*пккминфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="33539-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33539-107">Указатель на структуру [**ккминфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) , содержащую сведения, используемые при слиянии.</span><span class="sxs-lookup"><span data-stu-id="33539-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="33539-108">*уфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="33539-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33539-109">Флаги, указывающие, как можно изменить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="33539-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="33539-110">Этот параметр использует значения КМФ, \_ \* описанные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="33539-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33539-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="33539-111">Remarks</span></span>

<span data-ttu-id="33539-112">Если элементы добавляются в контекстное меню, они должны поддерживаться с подпрограммыми, которые отвечают соответствующим образом, когда один из этих элементов вызывается с помощью [**DFM \_ инвокекомманд**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="33539-112">If items are added to the context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="33539-113">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации объекта контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="33539-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="33539-114">Существует два интерфейса API для реализации, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="33539-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="33539-115">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="33539-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="33539-116">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="33539-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="33539-117">Требования</span><span class="sxs-lookup"><span data-stu-id="33539-117">Requirements</span></span>



| <span data-ttu-id="33539-118">Требование</span><span class="sxs-lookup"><span data-stu-id="33539-118">Requirement</span></span> | <span data-ttu-id="33539-119">Значение</span><span class="sxs-lookup"><span data-stu-id="33539-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33539-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33539-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33539-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33539-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="33539-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33539-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33539-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33539-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="33539-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="33539-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33539-125"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="33539-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





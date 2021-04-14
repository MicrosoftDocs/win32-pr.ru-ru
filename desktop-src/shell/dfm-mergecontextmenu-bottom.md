---
description: Разрешает обратный вызов для добавления элементов в нижнюю часть расширенного меню.
title: Сообщение DFM_MERGECONTEXTMENU_BOTTOM (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9274a36f531e53f86d05adab20b4970ea5ace84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984301"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a><span data-ttu-id="3fd90-103">\_Сообщение DFM мержеконтекстмену \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="3fd90-103">DFM\_MERGECONTEXTMENU\_BOTTOM message</span></span>

<span data-ttu-id="3fd90-104">Разрешает обратный вызов для добавления элементов в нижнюю часть расширенного меню.</span><span class="sxs-lookup"><span data-stu-id="3fd90-104">Allows the callback to add items to the bottom of the extended menu.</span></span>


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="3fd90-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fd90-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd90-106">*пккминфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fd90-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd90-107">Указатель на структуру [**ккминфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) , содержащую сведения, используемые при слиянии.</span><span class="sxs-lookup"><span data-stu-id="3fd90-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="3fd90-108">*уфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fd90-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd90-109">Флаги, указывающие, как можно изменить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="3fd90-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="3fd90-110">Этот параметр использует значения КМФ, \_ \* описанные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3fd90-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fd90-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3fd90-111">Remarks</span></span>

<span data-ttu-id="3fd90-112">Если элементы добавляются в расширенное контекстное меню, они должны поддерживаться с подпрограммыми, которые отвечают соответствующим образом, когда один из этих элементов вызывается с помощью [**DFM \_ инвокекомманд**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="3fd90-112">If items are added to the extended context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="3fd90-113">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fd90-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="3fd90-114">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3fd90-114">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="3fd90-115">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3fd90-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="3fd90-116">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="3fd90-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd90-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3fd90-117">Requirements</span></span>



| <span data-ttu-id="3fd90-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3fd90-118">Requirement</span></span> | <span data-ttu-id="3fd90-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3fd90-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd90-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fd90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd90-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fd90-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3fd90-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fd90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd90-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fd90-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3fd90-124">Header</span><span class="sxs-lookup"><span data-stu-id="3fd90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd90-125"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd90-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





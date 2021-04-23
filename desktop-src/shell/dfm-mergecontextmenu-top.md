---
description: Разрешает обратный вызов для добавления элементов в верхнюю часть расширенного меню.
title: Сообщение DFM_MERGECONTEXTMENU_TOP (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eed6aec6-11a0-4738-b5b9-a455d0e35eac
api_name:
- DFM_MERGECONTEXTMENU_TOP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5810b5b6a0fc862b4dd8a9605cb9aa5c0c83afc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540498"
---
# <a name="dfm_mergecontextmenu_top-message"></a><span data-ttu-id="b67d7-103">\_Сообщение DFM мержеконтекстмену \_ Top</span><span class="sxs-lookup"><span data-stu-id="b67d7-103">DFM\_MERGECONTEXTMENU\_TOP message</span></span>

<span data-ttu-id="b67d7-104">Разрешает обратный вызов для добавления элементов в верхнюю часть расширенного меню.</span><span class="sxs-lookup"><span data-stu-id="b67d7-104">Allows the callback to add items to the top of the extended menu.</span></span>


```C++
DFM_MERGECONTEXTMENU_TOP

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="b67d7-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b67d7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b67d7-106">*пккминфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b67d7-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d7-107">Указатель на структуру [**ккминфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) , содержащую сведения, используемые при слиянии.</span><span class="sxs-lookup"><span data-stu-id="b67d7-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="b67d7-108">*уфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b67d7-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d7-109">Флаги, указывающие, как можно изменить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="b67d7-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="b67d7-110">Этот параметр использует значения КМФ, \_ \* описанные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b67d7-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b67d7-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b67d7-111">Remarks</span></span>

<span data-ttu-id="b67d7-112">Если элементы добавляются в расширенное контекстное меню, они должны поддерживаться с подпрограммыми, которые отвечают соответствующим образом, когда один из этих элементов вызывается с помощью [**DFM \_ инвокекомманд**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="b67d7-112">If items are added to the extended context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="b67d7-113">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации объекта контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b67d7-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="b67d7-114">Существует два интерфейса API для реализации, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b67d7-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="b67d7-115">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b67d7-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="b67d7-116">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="b67d7-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b67d7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b67d7-117">Requirements</span></span>



| <span data-ttu-id="b67d7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b67d7-118">Requirement</span></span> | <span data-ttu-id="b67d7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b67d7-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b67d7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b67d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b67d7-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b67d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b67d7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b67d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b67d7-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b67d7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b67d7-124">Header</span><span class="sxs-lookup"><span data-stu-id="b67d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b67d7-125"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="b67d7-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





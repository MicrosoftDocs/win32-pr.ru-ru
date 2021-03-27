---
description: Отправка для проверки существования команды меню.
title: Сообщение DFM_VALIDATECMD (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143957"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="a3437-103">\_Сообщение DFM валидатекмд</span><span class="sxs-lookup"><span data-stu-id="a3437-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="a3437-104">Отправка для проверки существования команды меню.</span><span class="sxs-lookup"><span data-stu-id="a3437-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="a3437-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3437-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3437-106">*идкмд*</span><span class="sxs-lookup"><span data-stu-id="a3437-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="a3437-107">Смещение идентификатора команды меню.</span><span class="sxs-lookup"><span data-stu-id="a3437-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="a3437-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3437-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a3437-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="a3437-109">Not used.</span></span> <span data-ttu-id="a3437-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a3437-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3437-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3437-111">Return value</span></span>

<span data-ttu-id="a3437-112">Возвращает \_ значение s ОК, если команда существует, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a3437-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3437-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3437-113">Remarks</span></span>

<span data-ttu-id="a3437-114">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3437-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="a3437-115">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="a3437-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="a3437-116">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a3437-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="a3437-117">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="a3437-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3437-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a3437-118">Requirements</span></span>



| <span data-ttu-id="a3437-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a3437-119">Requirement</span></span> | <span data-ttu-id="a3437-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a3437-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3437-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3437-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a3437-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3437-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a3437-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3437-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a3437-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3437-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a3437-125">Header</span><span class="sxs-lookup"><span data-stu-id="a3437-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3437-126"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3437-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





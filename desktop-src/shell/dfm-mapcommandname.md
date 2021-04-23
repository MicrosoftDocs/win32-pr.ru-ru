---
description: Отправляется реализацией контекстного меню по умолчанию для назначения имени команде меню.
title: Сообщение DFM_MAPCOMMANDNAME (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540503"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="80143-103">\_Сообщение DFM мапкомманднаме</span><span class="sxs-lookup"><span data-stu-id="80143-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="80143-104">Отправляется реализацией контекстного меню по умолчанию для назначения имени команде меню.</span><span class="sxs-lookup"><span data-stu-id="80143-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="80143-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="80143-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80143-106">*дефаултид* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="80143-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80143-107">Указатель на идентификатор выбранной команды меню.</span><span class="sxs-lookup"><span data-stu-id="80143-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="80143-108">*псзкомманднаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80143-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80143-109">Указатель на строку в Юникоде, содержащую имя команды.</span><span class="sxs-lookup"><span data-stu-id="80143-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80143-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="80143-110">Remarks</span></span>

<span data-ttu-id="80143-111">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации объекта контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80143-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="80143-112">Существует два интерфейса API для реализации, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="80143-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="80143-113">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="80143-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="80143-114">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="80143-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="80143-115">Требования</span><span class="sxs-lookup"><span data-stu-id="80143-115">Requirements</span></span>



| <span data-ttu-id="80143-116">Требование</span><span class="sxs-lookup"><span data-stu-id="80143-116">Requirement</span></span> | <span data-ttu-id="80143-117">Значение</span><span class="sxs-lookup"><span data-stu-id="80143-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="80143-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80143-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80143-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80143-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="80143-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80143-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80143-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80143-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="80143-122">Header</span><span class="sxs-lookup"><span data-stu-id="80143-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80143-123"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="80143-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





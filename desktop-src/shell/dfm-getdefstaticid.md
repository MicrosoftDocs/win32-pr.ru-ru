---
description: Отправляется реализацией контекстного меню по умолчанию во время создания, с указанием команды меню по умолчанию и разрешающей выбор другого варианта. Используется ЛПФНДФМКАЛЛБАКК.
title: Сообщение DFM_GETDEFSTATICID (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423709"
---
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="c9668-104">\_Сообщение DFM жетдефстатиЦид</span><span class="sxs-lookup"><span data-stu-id="c9668-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="c9668-105">Отправляется реализацией контекстного меню по умолчанию во время создания, с указанием команды меню по умолчанию и разрешающей выбор другого варианта.</span><span class="sxs-lookup"><span data-stu-id="c9668-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="c9668-106">Используется [**лпфндфмкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span><span class="sxs-lookup"><span data-stu-id="c9668-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="c9668-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9668-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9668-108">*дефаултид* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c9668-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9668-109">Указатель на идентификатор выбранной команды меню.</span><span class="sxs-lookup"><span data-stu-id="c9668-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="c9668-110">Распознается следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="c9668-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="c9668-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Свойства cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="c9668-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="c9668-112">Отображение пользовательского интерфейса **свойств** для элемента, для которого было вызвано меню.</span><span class="sxs-lookup"><span data-stu-id="c9668-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9668-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9668-113">Remarks</span></span>

<span data-ttu-id="c9668-114">Чтобы переопределить выбор по умолчанию, обработчик должен при получении этого сообщения установить значение, на которое указывает *дефаултид* , на идентификатор команды замены и вернуть \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c9668-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="c9668-115">В противном случае возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9668-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="c9668-116">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9668-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="c9668-117">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="c9668-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="c9668-118">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c9668-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="c9668-119">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="c9668-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9668-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c9668-120">Requirements</span></span>



| <span data-ttu-id="c9668-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c9668-121">Requirement</span></span> | <span data-ttu-id="c9668-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c9668-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9668-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9668-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c9668-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9668-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c9668-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9668-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c9668-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9668-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9668-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c9668-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9668-128"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9668-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

---
description: Отправляется реализацией контекстного меню по умолчанию для запроса функции обратного вызова, которая обрабатывает меню (ЛПФНДФМКАЛЛБАКК) для вызова команды меню.
title: Сообщение DFM_INVOKECOMMAND (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984305"
---
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="124b6-103">\_Сообщение DFM инвокекомманд</span><span class="sxs-lookup"><span data-stu-id="124b6-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="124b6-104">Отправляется реализацией контекстного меню по умолчанию для запроса функции обратного вызова, которая обрабатывает меню ([**лпфндфмкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) для вызова команды меню.</span><span class="sxs-lookup"><span data-stu-id="124b6-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="124b6-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="124b6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124b6-106">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="124b6-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="124b6-107">Идентификатор команды выбранной команды меню.</span><span class="sxs-lookup"><span data-stu-id="124b6-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="124b6-108">Распознаются следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="124b6-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="124b6-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="124b6-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-110">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-110">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-111">Удаление текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="124b6-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="124b6-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_Перемещение DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="124b6-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-113">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-113">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-114">Переместить текущий элемент.</span><span class="sxs-lookup"><span data-stu-id="124b6-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="124b6-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_копирование DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="124b6-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-116">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-116">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-117">Копирование текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="124b6-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="124b6-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**Ссылка на DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="124b6-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-119">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-119">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-120">Создать ссылку на текущий элемент.</span><span class="sxs-lookup"><span data-stu-id="124b6-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="124b6-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Свойства cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="124b6-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-122">Отображение пользовательского интерфейса **свойств** для элемента, на котором было вызвано меню.</span><span class="sxs-lookup"><span data-stu-id="124b6-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="124b6-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="124b6-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="124b6-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="124b6-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd, \_ Вставка**</span><span class="sxs-lookup"><span data-stu-id="124b6-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-126">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-126">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-127">Вставка элемента в текущее расположение.</span><span class="sxs-lookup"><span data-stu-id="124b6-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="124b6-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ виевлист**</span><span class="sxs-lookup"><span data-stu-id="124b6-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-129">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="124b6-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="124b6-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ виевдетаилс**</span><span class="sxs-lookup"><span data-stu-id="124b6-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-131">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="124b6-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="124b6-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ пастелинк**</span><span class="sxs-lookup"><span data-stu-id="124b6-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-133">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-133">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-134">Вставка ссылки в текущее расположение.</span><span class="sxs-lookup"><span data-stu-id="124b6-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="124b6-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="124b6-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-136">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="124b6-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="124b6-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ модалпроп**</span><span class="sxs-lookup"><span data-stu-id="124b6-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-138">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="124b6-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="124b6-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_Переименовать DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="124b6-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="124b6-140">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="124b6-140">**Windows Vista and later**.</span></span> <span data-ttu-id="124b6-141">Переименование текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="124b6-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="124b6-142">*args* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="124b6-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="124b6-143">Указатель на строку, завершающуюся нулем, которая содержит дополнительные аргументы для выбранной команды меню.</span><span class="sxs-lookup"><span data-stu-id="124b6-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="124b6-144">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="124b6-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124b6-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="124b6-145">Return value</span></span>

<span data-ttu-id="124b6-146">Обработчик для этого сообщения должен вернуть \_ значение S false, если необходимо, чтобы реализация по умолчанию вызывала обработчик по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="124b6-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="124b6-147">Возврат \_ ОК, если сообщение было обработано.</span><span class="sxs-lookup"><span data-stu-id="124b6-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="124b6-148">В противном случае возвращается стандартный код ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="124b6-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="124b6-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="124b6-149">Remarks</span></span>

<span data-ttu-id="124b6-150">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="124b6-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="124b6-151">Существует два API для создания обратного вызова, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , который принимает указатель на функцию обратного вызова или [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , использующий объект обратного вызова, который поддерживает [**иконтекстменукб**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="124b6-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="124b6-152">Элементы, для которых вызывается команда, предоставляются в объекте данных, переданном в функцию обратного вызова или в метод [**иконтекстменукб:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="124b6-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="124b6-153">Этот объект данных предоставляется источником данных, который реализует обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="124b6-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="124b6-154">Чтобы извлечь элементы из объекта данных, используйте [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="124b6-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="124b6-155">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="124b6-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="124b6-156">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="124b6-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="124b6-157">Требования</span><span class="sxs-lookup"><span data-stu-id="124b6-157">Requirements</span></span>



| <span data-ttu-id="124b6-158">Требование</span><span class="sxs-lookup"><span data-stu-id="124b6-158">Requirement</span></span> | <span data-ttu-id="124b6-159">Значение</span><span class="sxs-lookup"><span data-stu-id="124b6-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="124b6-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="124b6-160">Minimum supported client</span></span><br/> | <span data-ttu-id="124b6-161">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="124b6-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="124b6-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="124b6-162">Minimum supported server</span></span><br/> | <span data-ttu-id="124b6-163">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="124b6-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="124b6-164">Заголовок</span><span class="sxs-lookup"><span data-stu-id="124b6-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="124b6-165"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="124b6-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

---
description: Отправляется реализацией контекстного меню по умолчанию, чтобы запросить ЛПФНДФМКАЛЛБАКК для вызова расширенной команды меню.
title: Сообщение DFM_INVOKECOMMANDEX (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540506"
---
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="e16c2-103">\_Сообщение DFM инвокекоммандекс</span><span class="sxs-lookup"><span data-stu-id="e16c2-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="e16c2-104">Отправляется реализацией контекстного меню по умолчанию, чтобы запросить [**лпфндфмкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) для вызова расширенной команды меню.</span><span class="sxs-lookup"><span data-stu-id="e16c2-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="e16c2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e16c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16c2-106">*идкмд* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e16c2-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16c2-107">Идентификатор команды выбранной команды меню.</span><span class="sxs-lookup"><span data-stu-id="e16c2-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="e16c2-108">Распознаются следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="e16c2-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="e16c2-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="e16c2-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="e16c2-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_Перемещение DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e16c2-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="e16c2-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_копирование DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e16c2-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="e16c2-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**Ссылка на DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e16c2-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="e16c2-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Свойства cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="e16c2-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="e16c2-114">Отображение пользовательского интерфейса **свойств** для элемента, для которого было вызвано меню.</span><span class="sxs-lookup"><span data-stu-id="e16c2-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="e16c2-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="e16c2-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="e16c2-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd, \_ Вставка**</span><span class="sxs-lookup"><span data-stu-id="e16c2-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="e16c2-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ виевлист**</span><span class="sxs-lookup"><span data-stu-id="e16c2-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="e16c2-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ виевдетаилс**</span><span class="sxs-lookup"><span data-stu-id="e16c2-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="e16c2-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ пастелинк**</span><span class="sxs-lookup"><span data-stu-id="e16c2-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="e16c2-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="e16c2-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="e16c2-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ модалпроп**</span><span class="sxs-lookup"><span data-stu-id="e16c2-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="e16c2-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_Переименовать DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e16c2-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e16c2-123">*Пдфмикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e16c2-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16c2-124">Указатель на структуру [**дфмикс**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) , которая содержит дополнительные аргументы для выбранной команды меню.</span><span class="sxs-lookup"><span data-stu-id="e16c2-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="e16c2-125">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e16c2-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e16c2-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="e16c2-126">Remarks</span></span>

<span data-ttu-id="e16c2-127">После получения этого сообщения функция должна вернуть \_ значение false, если необходимо, чтобы реализация по умолчанию вызывала обработчик по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="e16c2-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="e16c2-128">Возврат \_ ОК, если сообщение было обработано.</span><span class="sxs-lookup"><span data-stu-id="e16c2-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="e16c2-129">В противном случае возвращается стандартный код ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e16c2-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="e16c2-130">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e16c2-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="e16c2-131">Существует два API для создания обратного вызова, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , который принимает указатель на функцию обратного вызова или [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , использующий объект обратного вызова, который поддерживает [**иконтекстменукб**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="e16c2-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="e16c2-132">Элементы, для которых вызывается команда, предоставляются в объекте данных, переданном в функцию обратного вызова или в метод [**иконтекстменукб:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="e16c2-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="e16c2-133">Этот объект данных предоставляется источником данных, который реализует обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="e16c2-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="e16c2-134">Чтобы извлечь элементы из объекта данных, используйте [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="e16c2-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="e16c2-135">[**DFM \_ ИНВОКЕКОММАНД**](dfm-invokecommand.md) — это более простая версия этого сообщения, которая не предоставляет в ответном вызове больше информации.</span><span class="sxs-lookup"><span data-stu-id="e16c2-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="e16c2-136">Используйте **DFM \_ инвокекомманд** , если дополнительные сведения, предоставляемые **DFM \_ инвокекоммандекс** , не требуются в реализации.</span><span class="sxs-lookup"><span data-stu-id="e16c2-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e16c2-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e16c2-137">Requirements</span></span>



| <span data-ttu-id="e16c2-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e16c2-138">Requirement</span></span> | <span data-ttu-id="e16c2-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e16c2-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e16c2-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e16c2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e16c2-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e16c2-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e16c2-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e16c2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e16c2-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e16c2-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e16c2-144">Header</span><span class="sxs-lookup"><span data-stu-id="e16c2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e16c2-145"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16c2-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

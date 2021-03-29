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
# <a name="dfm_invokecommand-message"></a>\_Сообщение DFM инвокекомманд

Отправляется реализацией контекстного меню по умолчанию для запроса функции обратного вызова, которая обрабатывает меню ([**лпфндфмкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) для вызова команды меню.


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор* \[ в\]
</dt> <dd>

Идентификатор команды выбранной команды меню. Распознаются следующие флаги:

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**


</dt> <dd>

**Windows Vista и более поздние версии**. Удаление текущего элемента.

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_Перемещение DFM cmd \_**


</dt> <dd>

**Windows Vista и более поздние версии**. Переместить текущий элемент.

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_копирование DFM cmd \_**


</dt> <dd>

**Windows Vista и более поздние версии**. Копирование текущего элемента.

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**Ссылка на DFM \_ cmd \_**


</dt> <dd>

**Windows Vista и более поздние версии**. Создать ссылку на текущий элемент.

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Свойства cmd \_ DFM**


</dt> <dd>

Отображение пользовательского интерфейса **свойств** для элемента, на котором было вызвано меню.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**


</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd, \_ Вставка**


</dt> <dd>

**Windows Vista и более поздние версии**. Вставка элемента в текущее расположение.

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ виевлист**


</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ виевдетаилс**


</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ пастелинк**


</dt> <dd>

**Windows Vista и более поздние версии**. Вставка ссылки в текущее расположение.

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**


</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ модалпроп**


</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_Переименовать DFM cmd \_**


</dt> <dd>

**Windows Vista и более поздние версии**. Переименование текущего элемента.

</dd> </dl> </dd> <dt>

*args* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит дополнительные аргументы для выбранной команды меню. Этот параметр может принимать значение **NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Обработчик для этого сообщения должен вернуть \_ значение S false, если необходимо, чтобы реализация по умолчанию вызывала обработчик по умолчанию для команды. Возврат \_ ОК, если сообщение было обработано. В противном случае возвращается стандартный код ошибки HRESULT.

## <a name="remarks"></a>Примечания

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации обратного вызова. Существует два API для создания обратного вызова, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , который принимает указатель на функцию обратного вызова или [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , использующий объект обратного вызова, который поддерживает [**иконтекстменукб**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).

Элементы, для которых вызывается команда, предоставляются в объекте данных, переданном в функцию обратного вызова или в метод [**иконтекстменукб:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) . Этот объект данных предоставляется источником данных, который реализует обратный вызов. Чтобы извлечь элементы из объекта данных, используйте [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова. Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 

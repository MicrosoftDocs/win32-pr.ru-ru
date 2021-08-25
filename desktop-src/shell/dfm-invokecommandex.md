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
ms.openlocfilehash: 2b8a7fd63aa4269ee265a4ae147c99fe394e8aad725f7134f8d62daf8ee9984b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943174"
---
# <a name="dfm_invokecommandex-message"></a>\_Сообщение DFM инвокекоммандекс

Отправляется реализацией контекстного меню по умолчанию, чтобы запросить [**лпфндфмкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) для вызова расширенной команды меню.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идкмд* \[ в\]
</dt> <dd>

Идентификатор команды выбранной команды меню. Распознаются следующие флаги.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_Перемещение DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_копирование DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**Ссылка на DFM \_ cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Свойства cmd \_ DFM**


</dt> <dd>

Отображение пользовательского интерфейса **свойств** для элемента, для которого было вызвано меню.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ cmd, \_ Вставка**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ cmd \_ виевлист**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ виевдетаилс**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ пастелинк**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ модалпроп**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_Переименовать DFM cmd \_**


</dt> <dd></dd> </dl> </dd> <dt>

*Пдфмикс* \[ окне\]
</dt> <dd>

Указатель на структуру [**дфмикс**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) , которая содержит дополнительные аргументы для выбранной команды меню. Этот параметр может принимать значение **NULL**.

</dd> </dl>

## <a name="remarks"></a>Remarks

После получения этого сообщения функция должна вернуть \_ значение false, если необходимо, чтобы реализация по умолчанию вызывала обработчик по умолчанию для команды. Возврат \_ ОК, если сообщение было обработано. В противном случае возвращается стандартный код ошибки HRESULT.

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации обратного вызова. Существует два API для создания обратного вызова, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , который принимает указатель на функцию обратного вызова или [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , использующий объект обратного вызова, который поддерживает [**иконтекстменукб**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).

Элементы, для которых вызывается команда, предоставляются в объекте данных, переданном в функцию обратного вызова или в метод [**иконтекстменукб:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) . Этот объект данных предоставляется источником данных, который реализует обратный вызов. Чтобы извлечь элементы из объекта данных, используйте [**шкреатешеллитемаррайфромдатаобжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ ИНВОКЕКОММАНД**](dfm-invokecommand.md) — это более простая версия этого сообщения, которая не предоставляет в ответном вызове больше информации. Используйте **DFM \_ инвокекомманд** , если дополнительные сведения, предоставляемые **DFM \_ инвокекоммандекс** , не требуются в реализации.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 

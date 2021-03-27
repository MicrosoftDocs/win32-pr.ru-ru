---
description: СФВМная \_ панель может быть изменена или недоступна.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Сообщение SFVM_GETPANE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998846"
---
# <a name="sfvm_getpane-message"></a>\_Сообщение сфвм

\[**Сфвм \_ Группа доступности доступна для** использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Позволяет объекту обратного вызова предоставлять панель строки состояния, в которой отображаются сведения о зоне Интернета. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*панеид* \[ окне\]
</dt> <dd>

Идентификатор запрошенной панели. Обычно это зона области \_ , но может принимать одно из следующих значений.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**ПАНЕЛЬ \_ нет**


</dt> <dd>

Нет области.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**\_зона области**


</dt> <dd>

Область зоны Интернета.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**\_Автономная работа с панелью**


</dt> <dd>

Автономная область.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**ПАНЕЛЬ \_ принтера**


</dt> <dd>

Панель «индикации печати».

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**\_SSL панели**


</dt> <dd>

Панель SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**Навигация по ПАНЕЛЯМ \_**


</dt> <dd>

Область навигации.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**\_ход выполнения панели**


</dt> <dd>

Панель индикатора выполнения.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**\_Конфиденциальность области**


</dt> <dd>

Панель «индикатор конфиденциальности».

</dd> </dl> </dd> <dt>

*панель* \[ заполняет\]
</dt> <dd>

Указатель на **DWORD** , содержащий номер панели.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 

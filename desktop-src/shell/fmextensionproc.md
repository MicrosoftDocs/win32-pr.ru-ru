---
description: Указывает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов для взаимодействия с расширением диспетчера файлов.
title: Функция обратного вызова Фмекстенсионпрок (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842245"
---
# <a name="fmextensionproc-callback-function"></a>Функция обратного вызова Фмекстенсионпрок

Указывает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов для взаимодействия с расширением диспетчера файлов.

## <a name="syntax"></a>Синтаксис


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Тип: **HWND**

Обработчик окна для диспетчера файлов. Расширение использует этот обработчик, чтобы указать родительское окно для любого диалогового окна или поля сообщения, которое оно должно отображать, а также для отправки сообщений запросов в Диспетчер файлов.

</dd> <dt>

*вмсг* 
</dt> <dd>

Тип: **слово**

Одно из следующих сообщений диспетчера файлов.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**от 1 до 99**


</dt> <dd>

Пользователь выбрал элемент из меню, предоставляемого расширением. Значение является идентификатором выбранного пункта меню.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**ФМЕВЕНТ \_ хелпменуитем**


</dt> <dd>

Пользователь нажал клавишу F1 при выборе меню расширения или элемента команды панели инструментов. Указывает, что расширение должно правильно вызывать **WinHelp** для элемента команды.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**ФМЕВЕНТ \_ HELPSTRING**


</dt> <dd>

Пользователь выбрал пункт меню или команду панели инструментов. Указывает, что расширение должно предоставить строку справки.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**ФМЕВЕНТ \_ инитмену**


</dt> <dd>

Пользователь выбрал меню расширения. Расширение должно инициализировать элементы в меню.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**ФМЕВЕНТ \_ Загрузка**


</dt> <dd>

Диспетчер файлов загружает библиотеку DLL расширения и запрашивает у библиотеки DLL сведения о меню, предоставленном библиотекой DLL.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**ФМЕВЕНТ \_ селчанже**


</dt> <dd>

Был изменен выбор в окне каталога **диспетчера файлов** или в окне **результатов поиска** .

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**ФМЕВЕНТ \_ тулбарлоад**


</dt> <dd>

Диспетчер файлов создает панель инструментов и запрашивает у библиотеки DLL расширения сведения о любой кнопке, которую библиотека DLL добавляет на панель инструментов.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**\_выгрузка фмевент**


</dt> <dd>

Диспетчер файлов выгружает библиотеку DLL расширения.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**ФМЕВЕНТ \_ пользовательское \_ обновление**


</dt> <dd>

Пользователь выбрал команду " **Обновить** " в меню " **окно** ". При необходимости расширение должно обновлять элементы в меню.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Тип: **Long**

Значение, зависящее от сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **Long**

Возвращает значение, зависящее от сообщения параметра *вмсг* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Фмекстенсионпрокв** (Юникод)<br/>                                          |



 

 





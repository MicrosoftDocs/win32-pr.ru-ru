---
description: Возвращает набор флагов, указывающих текущие параметры представления.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Свойство Шеллфолдервиев. Виевоптионс (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997863"
---
# <a name="shellfolderviewviewoptions-property"></a>Шеллфолдервиев. Виевоптионс, свойство

Возвращает набор флагов, указывающих текущие параметры представления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a>Значение свойства

Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект параметров представления. Содержит одно или несколько из следующих значений:

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**Сфвво \_ ШОВАЛЛОБЖЕКТС** (0x00000001)


</dt> <dd>

Параметр " **Показывать все файлы** " включен.

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**Сфвво \_ ШОВЕКСТЕНСИОНС** (0x00000002)


</dt> <dd>

Параметр **Скрыть расширения для известных типов файлов** отключен.

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**Сфвво \_ ШОВКОМПКОЛОР** (0x00000008)


</dt> <dd>

Параметр **Отображать сжатые файлы и папки с дополнительным цветом** включен.

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**Сфвво \_ ШОВСИСФИЛЕС** (0x00000020)


</dt> <dd>

Параметр **не показывать скрытые файлы** включен.

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**Сфвво \_ WIN95CLASSIC** (0x00000040)


</dt> <dd>

Включен параметр " **классический стиль** ".

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**Сфвво \_ ДАУБЛЕКЛИККИНВЕБВИЕВ** (0x00000080)


</dt> <dd>

Параметр **двойной щелчок для открытия элемента** включен.

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**Сфвво \_ ДЕСКТОФТМЛ** (0x00000200)


</dt> <dd>

Включен параметр " **Активный рабочий стол — Просмотр в виде веб-страницы** ".

</dd> </dl>

## <a name="remarks"></a>Примечания

[**Фокуседитем**](shellfolderview-focuseditem.md) может быть вызван только в локальной системе. Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого метода в JScript Embedded в HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 

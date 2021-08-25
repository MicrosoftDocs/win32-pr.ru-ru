---
title: Создание элементов управления SysLink
description: Вы реализуете гиперссылки элемента управления SysLink через разметку в строке инициализации элемента управления или отправляете \_ сообщение LM сетитем.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b50e364a2701d52aa0ed62222b0901a66b6c4073891b7f9348fffc8997fdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878514"
---
# <a name="how-to-create-syslink-controls"></a>Создание элементов управления SysLink

Вы реализуете гиперссылки элемента управления SysLink через разметку в строке инициализации элемента управления или отправляете сообщение [**LM \_ сетитем**](lm-setitem.md) .

> [!Note]  
> Перед созданием элементов управления SysLink необходимо вызвать функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , указав \_ класс компоновки ICC \_ .

 

Чтобы создать SysLink, вызовите функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав класс окна [**\_ связи WC**](common-control-window-classes.md) . Параметр *лпвиндовнаме* , который является общим для этих функций, указывает указатель на строку, завершающуюся нулем, которая содержит помеченный текст для вывода. Стили окон, определенные для элементов управления SysLink, см. в разделе [стили элементов управления Syslink](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="create-a-syslink-control"></a>Создание элемента управления SysLink

В следующем примере кода создается элемент управления SysLink, отображающий две гиперссылки. Первая гиперссылка является URL-адресом в Интернете, а вторая — определяемой приложением.


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a>Remarks

Предполагается, что [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) уже вызван.

Указание стиля [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) гарантирует, что пользователь сможет выбрать ссылку с помощью перехода по ссылкам и нажать клавишу ВВОД.

Версия 6 ComCtl32.dll поддерживает только Юникод. Таким образом, нельзя создавать ANSI-версии элементов управления SysLink — только Юникод.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
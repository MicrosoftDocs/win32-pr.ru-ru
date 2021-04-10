---
title: Создание элементов управления с богатыми возможностями редактирования
description: Чтобы создать элемент управления Rich Edit, вызовите функцию CreateWindowEx, указав класс окна редактирования Rich.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070672"
---
# <a name="how-to-create-rich-edit-controls"></a>Создание элементов управления с богатыми возможностями редактирования

Чтобы создать элемент управления Rich Edit, вызовите функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав класс окна редактирования Rich. Для Microsoft Rich Edit 4,1 (Msftedit.dll) укажите класс МСФТЕДИТ в \_ качестве класса окна. Для всех предыдущих версий укажите класс RICHEDIT \_ . Дополнительные сведения см. в разделе [версии расширенного редактирования](about-rich-edit-controls.md).

Широкие возможности управления редактированием поддерживают большинство стилей окон, используемых с элементами управления "поле ввода", а также дополнительными стилями. Если необходимо разрешить несколько строк текста в элементе управления, следует указать [**\_ Многострочный**](edit-control-styles.md) стиль многостраничного окна ES. Дополнительные сведения см. в разделе [стили элементов управления Rich Edit](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="create-a-rich-edit-control"></a>Создание элемента управления Rich Edit

Следующий пример функции создает элемент управления Rich Edit и инициализирует его текстом.


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



В Microsoft Visual Studio 2005 и более поздних версиях можно добавить элемент управления Rich Edit в шаблон диалогового окна, перетащив элемент управления из панели элементов. Однако при этом в редакторе диалоговых окон не гарантируется, что нужная библиотека будет загружена перед созданием элемента управления. Чтобы загрузить Riched32.dll, Riched20.dll или Msftedit.dll перед созданием диалогового окна, необходимо вызвать функцию [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .

## <a name="remarks"></a>Комментарии

Чтобы использовать стили оформления с этими элементами управления, приложение должно включать манифест и вызывать функцию [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) в начале программы. Сведения о визуальных стилях см. в разделе [стили визуальных](themes-overview.md)элементов. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
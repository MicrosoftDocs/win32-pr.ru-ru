---
title: Предоставление безоконного редактирования элементов управления с помощью функций окна
description: Функциональные возможности окна включают возможность получения сообщений и владение контекстом устройства для рисования. Элементы управления Rich Edit без оконного редактирования получают эту функцию посредством пары интерфейсов Итекстсервицес и Итекссост.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce68a9e4e186be79e8f62cb009748916725e4af4f67d6522ed5eb47a92f33fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698604"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Предоставление безоконного редактирования элементов управления с помощью функций окна

Функциональные возможности окна включают возможность получения сообщений и владение контекстом устройства для рисования. Элементы управления Rich Edit без оконного редактирования получают эту функцию посредством пары интерфейсов: [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) и [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="establish-the-window-functionality"></a>Установить функциональные возможности окна

В следующем примере кода показано, как создать текстовый узел и текстовые службы.


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a>Remarks

Параметр *хмодричедит* в примере кода является обработчиком для модуля Msftedit.dll, и предполагается, что этот обработчик уже был извлечен вызовом функции **Ошибка GetModuleHandle** .

## <a name="complete-example"></a>Полный пример

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование безоконных элементов управления "поле ввода"](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





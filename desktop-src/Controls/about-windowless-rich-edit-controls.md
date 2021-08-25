---
title: О безоконном редактировании элементов управления
description: Безоконный элемент управления "поле ввода", также называемый объектом текстовых служб, является объектом, предоставляющим функциональные возможности элемента управления Rich Edit без предоставления окна.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b68a2bc0317a884f0516b73b3674d104c4fa6c12f16bdc24960d7ea0ef8bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922184"
---
# <a name="about-windowless-rich-edit-controls"></a>О безоконном редактировании элементов управления

Безоконный элемент управления "поле ввода", также называемый объектом текстовых служб, является объектом, предоставляющим функциональные возможности [элемента управления Rich Edit](rich-edit-controls.md) без предоставления окна. Чтобы обеспечить функциональные возможности окна, например возможность получения сообщений и контекста устройства, в котором он может рисовать, элементы управления безоконное редактирование используют пару интерфейсов: [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) и [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Чтобы создать безоконный элемент управления "поле ввода", вызовите функцию [**креатетекстсервицес**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) с указателем на реализацию интерфейса [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) . **Креатетекстсервицес** возвращает указатель [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , который можно запросить для получения указателя на реализацию [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) для элемента управления без окон.

Msftedit.dll экспортирует идентификатор интерфейса (IID) с именем **IID \_ итекстсервицес** , который можно использовать для запроса указателя [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) для интерфейса [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . В следующем примере показано, как получить **\_ итекстсервицес IID** и использовать его для получения интерфейса **итекстсервицес** .


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



Msftedit.dll также экспортирует идентификатор интерфейса (IID) с именем **IID \_ итекссост** , который можно использовать аналогичным образом для запроса интерфейса [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .

Интерфейс [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) содержит методы, управляющие вызовами безоконного вызова для получения сведений о вашем окне. Например, объект текстовых служб вызывает метод [**тксжетдк**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) для получения контекста устройства, в котором он может рисовать. Безоконный элемент управления вызывает метод [**ткснотифи**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) для отправки уведомлений, таких как подробные сообщения уведомления об изменении, на узел текста. Объект служб Text Services вызывает другие методы **итекссост** для запроса размещения текста для выполнения других служб, связанных с окном. Например, метод [**тксинвалидатерект**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) запрашивает у узла текста Добавление прямоугольника в область обновления окна.

Стандартный расширенный элемент управления "поле ввода" содержит процедуру окна, которая обрабатывает системные сообщения и сообщения из приложения. Можно использовать маркер окна элемента управления для отправки ИТ сообщений для выполнения редактирования текста и других операций. Но в безоконном элементе управления "поле ввода" не предусмотрена процедура окна для получения и обработки сообщений. Вместо этого он предоставляет интерфейс [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . Чтобы отправить сообщения в безоконный элемент управления "поле ввода", вызовите метод [**ткссендмессаже**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) . Этот метод можно использовать для отправки любого из сообщений с богатыми возможностями редактирования или передачи другим сообщениям, влияющим на элемент управления, например системных сообщений для ввода с клавиатуры или мыши.

Также можно создать объект текстовых служб как часть [статистического объекта COM](/windows/desktop/com/aggregation). Это упрощает статистическую обработку объекта текстовых служб с помощью объекта модели COM.

 

 
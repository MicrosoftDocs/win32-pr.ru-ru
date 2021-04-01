---
title: Использование OLE в элементах управления Rich Edit
description: В этом разделе содержатся сведения об использовании связывания и внедрения объектов (OLE) в элементах управления Rich Edit.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104133614"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Использование OLE в элементах управления Rich Edit

В этом разделе содержатся сведения об использовании связывания и внедрения объектов (OLE) в элементах управления Rich Edit.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="use-a-rich-edit-interface"></a>Использование расширенного интерфейса редактирования

Элементы управления Rich Edit предоставляют некоторые из своих функций через интерфейсы модели COM. Получая интерфейс из элемента управления, вы получаете возможность работать с другими объектами в элементе управления. Этот интерфейс можно получить, отправив сообщение [**EM \_ жетолеинтерфаце**](em-getoleinterface.md) . В интерфейсе [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) можно получить интерфейсы, используемые в [объектной модели текста](text-object-model.md).

Другой интерфейс, [**иричедитолекаллбакк**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), реализуется приложениями для определения поведения элемента управления, когда он взаимодействует с объектами.

### <a name="insert-an-object-into-a-rich-edit-control"></a>Вставка объекта в элемент управления Rich Edit

В следующем примере кода объект File вставляется в форматируемый элемент управления Edit. Если программа связана с типом файлов на компьютере пользователя (например, Microsoft Excel для XLS-файла), содержимое файла отображается в элементе управления. в противном случае отображается значок.

1.  Получите интерфейс [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) .

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Создайте структурированное хранилище.

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  Настройте формат данных.

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  Получение указателя на сайт для просмотра.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Создайте объект и извлеките его интерфейс **IUnknown** .

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  Получите интерфейс Иолеобжект для объекта.

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Чтобы обеспечить правильную инвентаризацию ссылок, уведомите объект, который он содержит.

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  Настройка сведений об объекте.

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  Переместить курсор в конец текста и добавить символ возврата каретки.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Вставьте объект.

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. Очистка.

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>Использование Иричедитолекаллбакк

Приложения реализуют интерфейс [**иричедитолекаллбакк**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) для реагирования на запросы, связанные с OLE, или действия, выполняемые элементом управления Rich Edit. Вы связываете реализацию интерфейса с элементом управления, отправляя сообщение [**EM \_ сетолекаллбакк**](em-setolecallback.md) . Затем элемент управления вызывает методы в вашей реализации интерфейса, если это уместно.

Например, [**куерякцептдата**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) вызывается, когда пользователь пытается перетащить или вставить объект в элемент управления. Если приложение может принимать данные, реализация метода возвращает значение S \_ ОК. в противном случае возвращается код ошибки. Метод также может выполнить некоторое другое действие, например предупреждение о том, что файлы этого типа не могут быть помещены в элемент управления.

## <a name="complete-insertobject-example-function"></a>Пример функции Complete Инсертобжект

В следующем примере кода показаны предыдущие фрагменты кода, Объединенные в одну полную функцию, которая включает в себя обработку ошибок.


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





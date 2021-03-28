---
description: Когда пользователь щелкает правой кнопкой мыши член типа файла для вывода страницы свойств свойства, оболочка вызывает обработчики страницы свойств, зарегистрированные для данного типа файлов. Каждый обработчик может добавить одну пользовательскую страницу в страницу свойств по умолчанию.
title: Регистрация и реализация обработчика страницы свойств для типа файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997699"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Регистрация и реализация обработчика страницы свойств для типа файла

Когда пользователь щелкает правой кнопкой мыши член типа файла для вывода страницы свойств свойства, оболочка вызывает обработчики страницы свойств, зарегистрированные для данного типа файлов. Каждый обработчик может добавить одну пользовательскую страницу в страницу свойств по умолчанию.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   Shell

### <a name="prerequisites"></a>Предварительные условия

-   Общие сведения о контекстных меню

## <a name="instructions"></a>Инструкции

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Шаг 1. регистрация обработчика страницы свойств для типа файла

Помимо обычной регистрации компонента COM, добавьте подраздел **пропертишисандлерс** в подраздел **шеллекс** ключа ProgID приложения, связанного с типом файла. Создайте подраздел **пропертишисандлерс** с именем обработчика и задайте значение по умолчанию в форме строки GUID идентификатора класса обработчика страницы свойств (CLSID).

Чтобы добавить на страницу свойств несколько страниц, зарегистрируйте обработчик для каждой страницы. Максимальное число страниц, которое может поддерживать страница свойств, — 32. Чтобы зарегистрировать несколько обработчиков, создайте ключ в разделе **шеллекс** для каждого обработчика со значением по умолчанию, равным GUID CLSID обработчика. Нет необходимости создавать отдельный объект для каждого обработчика, что означает, что все обработчики могут иметь одинаковое значение GUID. Страницы будут отображаться в том порядке, в котором их ключи перечислены в разделе **шеллекс**.

В следующем примере показана запись реестра, которая включает два обработчика расширения страницы свойств для типа файла example. МИП. В этом примере для каждой страницы используется отдельный объект, но для обоих можно использовать и один объект.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Шаг 2. Реализация обработчика страницы свойств для типа файла

В дополнение к общей реализации, описанной в разделе [работа обработчиков страницы свойств](propsheet-handlers.md), обработчик страницы свойств для типа файла должен также иметь соответствующую реализацию интерфейса [**ишеллпропшитекст**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Только методу [**ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) требуется реализация, не которая является маркером. Оболочка не вызывает [**ишеллпропшитекст:: реплацепаже**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

Метод [**ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) позволяет обработчику страницы свойств добавить страницу к странице свойств. Метод имеет два входных параметра. Первый, *лпфнаддпаже*, является указателем на функцию обратного вызова [*аддпропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) , которая используется для предоставления командной консоли сведений, необходимых для добавления страницы на страницу свойств. Второе, *lParam*, — это значение, определяемое оболочкой, которое не обрабатывается обработчиком. Он просто передается обратно в оболочку при вызове функции обратного вызова.

Общая процедура реализации [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) выглядит следующим образом.

**Реализация метода Аддпажес**

1.  Присвойте соответствующие значения элементам структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) . В частности:
    -   Назначьте переменную, которая содержит счетчик ссылок обработчика, на элемент **пкрефпарент** . Эта практика предотвращает выгрузку объекта обработчика, пока страница свойств все еще отображается.
    -   Можно также реализовать функцию обратного вызова [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) и назначить ее указатель на элемент **пфнкаллбакк** . Эта функция вызывается при создании страницы и при ее уничтожении.
2.  Создайте обработчик ХПАЖЕ страницы, передав структуру [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) в функцию [**креатепропертишитпаже**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .
3.  Вызовите функцию, на которую указывает *лпфнаддпаже*. Присвойте его первому параметру маркер ХПАЖЕ, созданный на предыдущем шаге. Задайте для второго параметра значение *lParam* , переданное в [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) оболочкой.
4.  Все сообщения, связанные со страницей, будут переданы в процедуру диалогового окна, которая была назначена элементу **пфндлгпрок** структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .
5.  Если для **пфнкаллбакк** была назначена функция обратного вызова [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) , она будет вызвана, когда страница собирается уничтожиться. Затем обработчик может выполнить все необходимые операции очистки, например освободить все содержащиеся в нем ссылки.

В следующем образце кода показана простая реализация [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



Переменная **g \_ хинст** — это экземпляр библиотеки DLL, а Идд \_ пажедлг — идентификатор ресурса шаблона диалогового окна страницы. Функция **пажедлгпрок** — это процедура диалогового окна, которая обрабатывает сообщения страницы. Переменная **g \_ дллрефкаунт** содержит счетчик ссылок объекта. Метод [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) вызывает [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) для увеличения числа. Однако счетчик ссылок освобождается функцией обратного вызова **пажекаллбаккпрок**, когда страница собирается уничтожиться.

## <a name="remarks"></a>Примечания

Общие сведения о регистрации обработчиков расширений оболочки см. в статье [Создание обработчиков расширений](handlers.md)оболочки.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ишеллпропшитекст**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 

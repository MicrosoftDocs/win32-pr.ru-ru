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
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="f0f64-104">Регистрация и реализация обработчика страницы свойств для типа файла</span><span class="sxs-lookup"><span data-stu-id="f0f64-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="f0f64-105">Когда пользователь щелкает правой кнопкой мыши член типа файла для вывода страницы свойств свойства, оболочка вызывает обработчики страницы свойств, зарегистрированные для данного типа файлов.</span><span class="sxs-lookup"><span data-stu-id="f0f64-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="f0f64-106">Каждый обработчик может добавить одну пользовательскую страницу в страницу свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0f64-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f0f64-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="f0f64-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f0f64-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="f0f64-108">Technologies</span></span>

-   <span data-ttu-id="f0f64-109">Shell</span><span class="sxs-lookup"><span data-stu-id="f0f64-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f0f64-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f0f64-110">Prerequisites</span></span>

-   <span data-ttu-id="f0f64-111">Общие сведения о контекстных меню</span><span class="sxs-lookup"><span data-stu-id="f0f64-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="f0f64-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f0f64-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="f0f64-113">Шаг 1. регистрация обработчика страницы свойств для типа файла</span><span class="sxs-lookup"><span data-stu-id="f0f64-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="f0f64-114">Помимо обычной регистрации компонента COM, добавьте подраздел **пропертишисандлерс** в подраздел **шеллекс** ключа ProgID приложения, связанного с типом файла.</span><span class="sxs-lookup"><span data-stu-id="f0f64-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="f0f64-115">Создайте подраздел **пропертишисандлерс** с именем обработчика и задайте значение по умолчанию в форме строки GUID идентификатора класса обработчика страницы свойств (CLSID).</span><span class="sxs-lookup"><span data-stu-id="f0f64-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="f0f64-116">Чтобы добавить на страницу свойств несколько страниц, зарегистрируйте обработчик для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="f0f64-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="f0f64-117">Максимальное число страниц, которое может поддерживать страница свойств, — 32.</span><span class="sxs-lookup"><span data-stu-id="f0f64-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="f0f64-118">Чтобы зарегистрировать несколько обработчиков, создайте ключ в разделе **шеллекс** для каждого обработчика со значением по умолчанию, равным GUID CLSID обработчика.</span><span class="sxs-lookup"><span data-stu-id="f0f64-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="f0f64-119">Нет необходимости создавать отдельный объект для каждого обработчика, что означает, что все обработчики могут иметь одинаковое значение GUID.</span><span class="sxs-lookup"><span data-stu-id="f0f64-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="f0f64-120">Страницы будут отображаться в том порядке, в котором их ключи перечислены в разделе **шеллекс**.</span><span class="sxs-lookup"><span data-stu-id="f0f64-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="f0f64-121">В следующем примере показана запись реестра, которая включает два обработчика расширения страницы свойств для типа файла example. МИП.</span><span class="sxs-lookup"><span data-stu-id="f0f64-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="f0f64-122">В этом примере для каждой страницы используется отдельный объект, но для обоих можно использовать и один объект.</span><span class="sxs-lookup"><span data-stu-id="f0f64-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

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

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="f0f64-123">Шаг 2. Реализация обработчика страницы свойств для типа файла</span><span class="sxs-lookup"><span data-stu-id="f0f64-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="f0f64-124">В дополнение к общей реализации, описанной в разделе [работа обработчиков страницы свойств](propsheet-handlers.md), обработчик страницы свойств для типа файла должен также иметь соответствующую реализацию интерфейса [**ишеллпропшитекст**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="f0f64-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="f0f64-125">Только методу [**ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) требуется реализация, не которая является маркером.</span><span class="sxs-lookup"><span data-stu-id="f0f64-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="f0f64-126">Оболочка не вызывает [**ишеллпропшитекст:: реплацепаже**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span><span class="sxs-lookup"><span data-stu-id="f0f64-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="f0f64-127">Метод [**ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) позволяет обработчику страницы свойств добавить страницу к странице свойств.</span><span class="sxs-lookup"><span data-stu-id="f0f64-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="f0f64-128">Метод имеет два входных параметра.</span><span class="sxs-lookup"><span data-stu-id="f0f64-128">The method has two input parameters.</span></span> <span data-ttu-id="f0f64-129">Первый, *лпфнаддпаже*, является указателем на функцию обратного вызова [*аддпропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) , которая используется для предоставления командной консоли сведений, необходимых для добавления страницы на страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="f0f64-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="f0f64-130">Второе, *lParam*, — это значение, определяемое оболочкой, которое не обрабатывается обработчиком.</span><span class="sxs-lookup"><span data-stu-id="f0f64-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="f0f64-131">Он просто передается обратно в оболочку при вызове функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f0f64-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="f0f64-132">Общая процедура реализации [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f0f64-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="f0f64-133">**Реализация метода Аддпажес**</span><span class="sxs-lookup"><span data-stu-id="f0f64-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="f0f64-134">Присвойте соответствующие значения элементам структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="f0f64-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="f0f64-135">В частности:</span><span class="sxs-lookup"><span data-stu-id="f0f64-135">In particular:</span></span>
    -   <span data-ttu-id="f0f64-136">Назначьте переменную, которая содержит счетчик ссылок обработчика, на элемент **пкрефпарент** .</span><span class="sxs-lookup"><span data-stu-id="f0f64-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="f0f64-137">Эта практика предотвращает выгрузку объекта обработчика, пока страница свойств все еще отображается.</span><span class="sxs-lookup"><span data-stu-id="f0f64-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="f0f64-138">Можно также реализовать функцию обратного вызова [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) и назначить ее указатель на элемент **пфнкаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="f0f64-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="f0f64-139">Эта функция вызывается при создании страницы и при ее уничтожении.</span><span class="sxs-lookup"><span data-stu-id="f0f64-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="f0f64-140">Создайте обработчик ХПАЖЕ страницы, передав структуру [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) в функцию [**креатепропертишитпаже**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="f0f64-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="f0f64-141">Вызовите функцию, на которую указывает *лпфнаддпаже*.</span><span class="sxs-lookup"><span data-stu-id="f0f64-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="f0f64-142">Присвойте его первому параметру маркер ХПАЖЕ, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="f0f64-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="f0f64-143">Задайте для второго параметра значение *lParam* , переданное в [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) оболочкой.</span><span class="sxs-lookup"><span data-stu-id="f0f64-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="f0f64-144">Все сообщения, связанные со страницей, будут переданы в процедуру диалогового окна, которая была назначена элементу **пфндлгпрок** структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="f0f64-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="f0f64-145">Если для **пфнкаллбакк** была назначена функция обратного вызова [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) , она будет вызвана, когда страница собирается уничтожиться.</span><span class="sxs-lookup"><span data-stu-id="f0f64-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="f0f64-146">Затем обработчик может выполнить все необходимые операции очистки, например освободить все содержащиеся в нем ссылки.</span><span class="sxs-lookup"><span data-stu-id="f0f64-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="f0f64-147">В следующем образце кода показана простая реализация [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .</span><span class="sxs-lookup"><span data-stu-id="f0f64-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


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



<span data-ttu-id="f0f64-148">Переменная **g \_ хинст** — это экземпляр библиотеки DLL, а Идд \_ пажедлг — идентификатор ресурса шаблона диалогового окна страницы.</span><span class="sxs-lookup"><span data-stu-id="f0f64-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="f0f64-149">Функция **пажедлгпрок** — это процедура диалогового окна, которая обрабатывает сообщения страницы.</span><span class="sxs-lookup"><span data-stu-id="f0f64-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="f0f64-150">Переменная **g \_ дллрефкаунт** содержит счетчик ссылок объекта.</span><span class="sxs-lookup"><span data-stu-id="f0f64-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="f0f64-151">Метод [**аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) вызывает [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) для увеличения числа.</span><span class="sxs-lookup"><span data-stu-id="f0f64-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="f0f64-152">Однако счетчик ссылок освобождается функцией обратного вызова **пажекаллбаккпрок**, когда страница собирается уничтожиться.</span><span class="sxs-lookup"><span data-stu-id="f0f64-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f64-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0f64-153">Remarks</span></span>

<span data-ttu-id="f0f64-154">Общие сведения о регистрации обработчиков расширений оболочки см. в статье [Создание обработчиков расширений](handlers.md)оболочки.</span><span class="sxs-lookup"><span data-stu-id="f0f64-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0f64-155">См. также</span><span class="sxs-lookup"><span data-stu-id="f0f64-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f64-156">**ишеллпропшитекст**</span><span class="sxs-lookup"><span data-stu-id="f0f64-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 

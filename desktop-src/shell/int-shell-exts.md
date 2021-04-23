---
description: Большая часть реализации объекта обработчика расширений оболочки определяется его типом. Однако есть некоторые распространенные элементы. В этом разделе обсуждаются аспекты реализации, совместно используемые всеми обработчиками расширений оболочки.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Инициализация обработчиков расширений оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986049"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="ae990-105">Инициализация обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="ae990-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="ae990-106">Большая часть реализации объекта обработчика расширений оболочки определяется его типом.</span><span class="sxs-lookup"><span data-stu-id="ae990-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="ae990-107">Однако есть некоторые распространенные элементы.</span><span class="sxs-lookup"><span data-stu-id="ae990-107">There are, however, some common elements.</span></span> <span data-ttu-id="ae990-108">В этом разделе обсуждаются аспекты реализации, совместно используемые всеми обработчиками расширений оболочки.</span><span class="sxs-lookup"><span data-stu-id="ae990-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="ae990-109">Все обработчики расширений оболочки — это объекты модели COM.</span><span class="sxs-lookup"><span data-stu-id="ae990-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="ae990-110">Им необходимо назначить идентификатор GUID и зарегистрировать, как описано в разделе [Регистрация обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ae990-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="ae990-111">Они реализуются в виде библиотек DLL и должны экспортировать следующие стандартные функции:</span><span class="sxs-lookup"><span data-stu-id="ae990-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="ae990-112">[**DllMain**](../dlls/dllmain.md).</span><span class="sxs-lookup"><span data-stu-id="ae990-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="ae990-113">Стандартная точка входа для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="ae990-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="ae990-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span><span class="sxs-lookup"><span data-stu-id="ae990-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="ae990-115">Предоставляет фабрику класса объекта.</span><span class="sxs-lookup"><span data-stu-id="ae990-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="ae990-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span><span class="sxs-lookup"><span data-stu-id="ae990-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="ae990-117">COM вызывает эту функцию, чтобы определить, обслуживает ли объект какие-либо клиенты.</span><span class="sxs-lookup"><span data-stu-id="ae990-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="ae990-118">В противном случае система может выгрузить библиотеку DLL и освободить связанную с ней память.</span><span class="sxs-lookup"><span data-stu-id="ae990-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="ae990-119">Как и все COM-объекты, обработчики расширений оболочки должны реализовывать интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и [фабрику классов](../com/implementing-iclassfactory.md).</span><span class="sxs-lookup"><span data-stu-id="ae990-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="ae990-120">В большинстве случаев также необходимо реализовать интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) или [**ИШЕЛЛЕКСТИНИТ**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) в Windows XP или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="ae990-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="ae990-121">Они были заменены на [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) и [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ae990-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="ae990-122">Оболочка использует эти интерфейсы для инициализации обработчика.</span><span class="sxs-lookup"><span data-stu-id="ae990-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="ae990-123">Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) должен быть реализован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae990-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="ae990-124">Обработчики значков</span><span class="sxs-lookup"><span data-stu-id="ae990-124">Icon handlers</span></span>
-   <span data-ttu-id="ae990-125">Обработчики данных</span><span class="sxs-lookup"><span data-stu-id="ae990-125">Data handlers</span></span>
-   <span data-ttu-id="ae990-126">Удалить обработчики</span><span class="sxs-lookup"><span data-stu-id="ae990-126">Drop handlers</span></span>

<span data-ttu-id="ae990-127">Интерфейс [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) должен быть реализован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae990-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="ae990-128">Обработчики контекстного меню</span><span class="sxs-lookup"><span data-stu-id="ae990-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="ae990-129">Обработчики перетаскивания</span><span class="sxs-lookup"><span data-stu-id="ae990-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="ae990-130">Обработчики страницы свойств</span><span class="sxs-lookup"><span data-stu-id="ae990-130">Property sheet handlers</span></span>

<span data-ttu-id="ae990-131">В оставшейся части этого раздела обсуждаются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="ae990-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="ae990-132">Реализация IPersistFile</span><span class="sxs-lookup"><span data-stu-id="ae990-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="ae990-133">Реализация Ишеллекстинит</span><span class="sxs-lookup"><span data-stu-id="ae990-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="ae990-134">Настройка всплывающей подсказки</span><span class="sxs-lookup"><span data-stu-id="ae990-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="ae990-135">См. также</span><span class="sxs-lookup"><span data-stu-id="ae990-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="ae990-136">Реализация IPersistFile</span><span class="sxs-lookup"><span data-stu-id="ae990-136">Implementing IPersistFile</span></span>

<span data-ttu-id="ae990-137">Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) предназначен для того, чтобы объект был загружен или сохранен в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="ae990-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="ae990-138">В нем есть шесть методов в дополнение к [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), пять его собственных и методу [**ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , который он наследует от [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span><span class="sxs-lookup"><span data-stu-id="ae990-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="ae990-139">С помощью расширений оболочки **IPersist** используется только для инициализации объекта обработчика расширений оболочки.</span><span class="sxs-lookup"><span data-stu-id="ae990-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="ae990-140">Так как обычно нет необходимости выполнять чтение или запись на диск, только для методов **класса** и метода [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) требуется только реализация без маркера.</span><span class="sxs-lookup"><span data-stu-id="ae990-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="ae990-141">Оболочка вызывает метод [**ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , а функция возвращает идентификатор класса (CLSID) объекта обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="ae990-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="ae990-142">Затем оболочка вызывает [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) и передает два значения.</span><span class="sxs-lookup"><span data-stu-id="ae990-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="ae990-143">Первая, *псзфиле*, представляет собой строку в Юникоде с именем файла или папки, в которой будет выполняться оболочка.</span><span class="sxs-lookup"><span data-stu-id="ae990-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="ae990-144">Второй — *двмоде*, который указывает режим доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="ae990-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="ae990-145">Так как обычно нет необходимости в доступе к файлам, *двмоде* обычно равен нулю.</span><span class="sxs-lookup"><span data-stu-id="ae990-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="ae990-146">Метод сохраняет эти значения в соответствии с последующими ссылками.</span><span class="sxs-lookup"><span data-stu-id="ae990-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="ae990-147">В следующем фрагменте кода показано, как типичный обработчик расширений оболочки реализует методы класса [**и метода-**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) [**ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) .</span><span class="sxs-lookup"><span data-stu-id="ae990-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="ae990-148">Он предназначен для работы с ANSI или Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae990-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="ae990-149">CLSID \_ сампликссандлер — это идентификатор GUID объекта обработчика расширений, а ксамплешеллекстенсион — имя класса, используемого для реализации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae990-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="ae990-150">Переменные **m \_ сзфиленаме** и **m \_ двмоде** являются частными переменными, которые используются для хранения имени файла и флагов доступа.</span><span class="sxs-lookup"><span data-stu-id="ae990-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="ae990-151">Реализация Ишеллекстинит</span><span class="sxs-lookup"><span data-stu-id="ae990-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="ae990-152">Помимо [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), в интерфейсе [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) имеется только один метод, [**ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize).</span><span class="sxs-lookup"><span data-stu-id="ae990-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="ae990-153">Метод имеет три параметра, которые оболочка может использовать для передачи различных типов данных.</span><span class="sxs-lookup"><span data-stu-id="ae990-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="ae990-154">Передаваемые значения зависят от типа обработчика, а некоторые могут иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ae990-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="ae990-155">*пидлфолдер* содержит указатель папки на список идентификаторов элементов (Пидл).</span><span class="sxs-lookup"><span data-stu-id="ae990-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="ae990-156">Это абсолютно ПИДЛ.</span><span class="sxs-lookup"><span data-stu-id="ae990-156">This is an absolute PIDL.</span></span> <span data-ttu-id="ae990-157">Для расширений таблицы свойств это значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="ae990-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="ae990-158">Для расширений контекстного меню это ПИДЛ папки, содержащей элемент, контекстное меню которого отображается.</span><span class="sxs-lookup"><span data-stu-id="ae990-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="ae990-159">Для обработчиков перетаскивания, не заданных по умолчанию, это ПИДЛ целевой папки.</span><span class="sxs-lookup"><span data-stu-id="ae990-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="ae990-160">*pDataObject* содержит указатель на интерфейс [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) объекта данных.</span><span class="sxs-lookup"><span data-stu-id="ae990-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="ae990-161">Объект данных содержит одно или несколько имен файлов в формате [CF \_ HDROP](dragdrop.md) .</span><span class="sxs-lookup"><span data-stu-id="ae990-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="ae990-162">*хрегкэй* содержит раздел реестра для объекта File или типа Folder.</span><span class="sxs-lookup"><span data-stu-id="ae990-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="ae990-163">Метод [**ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) сохраняет имя файла, указатель [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) и раздел реестра, необходимые для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="ae990-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="ae990-164">В следующем фрагменте кода показана реализация **ишеллекстинит:: Initialize**.</span><span class="sxs-lookup"><span data-stu-id="ae990-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="ae990-165">Для простоты в этом примере предполагается, что объект данных содержит только один файл.</span><span class="sxs-lookup"><span data-stu-id="ae990-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="ae990-166">Как правило, объект данных может содержать несколько файлов, каждый из которых необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="ae990-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="ae990-167">Настройка всплывающей подсказки</span><span class="sxs-lookup"><span data-stu-id="ae990-167">Infotip Customization</span></span>

<span data-ttu-id="ae990-168">Существует два способа настройки инфотипс.</span><span class="sxs-lookup"><span data-stu-id="ae990-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="ae990-169">Один из способов — реализовать объект, который поддерживает [**икуеринфо**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) , а затем зарегистрировать объект в соответствующем подразделе реестра (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="ae990-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="ae990-170">Кроме того, можно указать либо фиксированную строку, либо список некоторых свойств файла для отображения.</span><span class="sxs-lookup"><span data-stu-id="ae990-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="ae990-171">Чтобы отобразить фиксированную строку для расширения пространства имен, создайте подраздел с именем **подсказки** под ключом CLSID расширения пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ae990-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="ae990-172">Установите данные этого подраздела в качестве строки, которую необходимо отобразить.</span><span class="sxs-lookup"><span data-stu-id="ae990-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="ae990-173">Чтобы отобразить фиксированную строку для типа файла, создайте подраздел с именем **подсказки** под ключом **ProgID** для типа файла, для которого вы хотите предоставить инфотипс.</span><span class="sxs-lookup"><span data-stu-id="ae990-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="ae990-174">Установите данные этого подраздела в качестве строки, которую необходимо отобразить.</span><span class="sxs-lookup"><span data-stu-id="ae990-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="ae990-175">Если требуется, чтобы оболочка отображала определенные свойства файла в подсказке для конкретного типа файлов, создайте **подсказку** под ключом **ProgID** для этого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="ae990-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="ae990-176">Установите данные этого подраздела в виде разделенного точкой с запятой списка канонических имен свойств или {fmtid}, пар PID, где *пропнаме* является каноническим именем свойства и *{fmtid}, PID* — это [**пара fmtid/PID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="ae990-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="ae990-177">Можно использовать следующие имена свойств.</span><span class="sxs-lookup"><span data-stu-id="ae990-177">The following property names can be used.</span></span>



| <span data-ttu-id="ae990-178">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="ae990-178">Property Name</span></span>    | <span data-ttu-id="ae990-179">Описание</span><span class="sxs-lookup"><span data-stu-id="ae990-179">Description</span></span>                   | <span data-ttu-id="ae990-180">Получено из</span><span class="sxs-lookup"><span data-stu-id="ae990-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae990-181">Автор</span><span class="sxs-lookup"><span data-stu-id="ae990-181">Author</span></span>           | <span data-ttu-id="ae990-182">Автор документа</span><span class="sxs-lookup"><span data-stu-id="ae990-182">Author of the document</span></span>        | [<span data-ttu-id="ae990-183">**\_Автор пидси**</span><span class="sxs-lookup"><span data-stu-id="ae990-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="ae990-184">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ae990-184">Title</span></span>            | <span data-ttu-id="ae990-185">Название документа</span><span class="sxs-lookup"><span data-stu-id="ae990-185">Title of the document</span></span>         | [<span data-ttu-id="ae990-186">**\_заголовок пидси**</span><span class="sxs-lookup"><span data-stu-id="ae990-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="ae990-187">Субъект</span><span class="sxs-lookup"><span data-stu-id="ae990-187">Subject</span></span>          | <span data-ttu-id="ae990-188">Сводка по теме</span><span class="sxs-lookup"><span data-stu-id="ae990-188">Subject summary</span></span>               | [<span data-ttu-id="ae990-189">**\_Тема пидси**</span><span class="sxs-lookup"><span data-stu-id="ae990-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="ae990-190">Комментировать</span><span class="sxs-lookup"><span data-stu-id="ae990-190">Comment</span></span>          | <span data-ttu-id="ae990-191">Комментарии к документу</span><span class="sxs-lookup"><span data-stu-id="ae990-191">Document comments</span></span>             | <span data-ttu-id="ae990-192">[**Пидси \_ Свойства комментария**](../stg/the-summary-information-property-set.md) или папки/диска</span><span class="sxs-lookup"><span data-stu-id="ae990-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="ae990-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="ae990-193">PageCount</span></span>        | <span data-ttu-id="ae990-194">Количество страниц</span><span class="sxs-lookup"><span data-stu-id="ae990-194">Number of pages</span></span>               | [<span data-ttu-id="ae990-195">**ПИДСИ \_ PAGECOUNT**</span><span class="sxs-lookup"><span data-stu-id="ae990-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="ae990-196">Имя</span><span class="sxs-lookup"><span data-stu-id="ae990-196">Name</span></span>             | <span data-ttu-id="ae990-197">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="ae990-197">Friendly name</span></span>                 | <span data-ttu-id="ae990-198">Стандартное представление папки</span><span class="sxs-lookup"><span data-stu-id="ae990-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="ae990-199">оригиналлокатион</span><span class="sxs-lookup"><span data-stu-id="ae990-199">OriginalLocation</span></span> | <span data-ttu-id="ae990-200">Расположение исходного файла</span><span class="sxs-lookup"><span data-stu-id="ae990-200">Location of original file</span></span>     | <span data-ttu-id="ae990-201">Папка "портфель" и папка "Корзина"</span><span class="sxs-lookup"><span data-stu-id="ae990-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="ae990-202">датеделетед</span><span class="sxs-lookup"><span data-stu-id="ae990-202">DateDeleted</span></span>      | <span data-ttu-id="ae990-203">Файл даты удален</span><span class="sxs-lookup"><span data-stu-id="ae990-203">Date file was deleted</span></span>         | <span data-ttu-id="ae990-204">Папка корзины</span><span class="sxs-lookup"><span data-stu-id="ae990-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="ae990-205">Тип</span><span class="sxs-lookup"><span data-stu-id="ae990-205">Type</span></span>             | <span data-ttu-id="ae990-206">Тип файла</span><span class="sxs-lookup"><span data-stu-id="ae990-206">Type of file</span></span>                  | <span data-ttu-id="ae990-207">Представление сведений о стандартной папке</span><span class="sxs-lookup"><span data-stu-id="ae990-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="ae990-208">Размер</span><span class="sxs-lookup"><span data-stu-id="ae990-208">Size</span></span>             | <span data-ttu-id="ae990-209">Размер файла</span><span class="sxs-lookup"><span data-stu-id="ae990-209">Size of file</span></span>                  | <span data-ttu-id="ae990-210">Представление сведений о стандартной папке</span><span class="sxs-lookup"><span data-stu-id="ae990-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="ae990-211">синккопин</span><span class="sxs-lookup"><span data-stu-id="ae990-211">SyncCopyIn</span></span>       | <span data-ttu-id="ae990-212">То же, что и Оригиналлокатион</span><span class="sxs-lookup"><span data-stu-id="ae990-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="ae990-213">То же, что и Оригиналлокатион</span><span class="sxs-lookup"><span data-stu-id="ae990-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="ae990-214">Изменен</span><span class="sxs-lookup"><span data-stu-id="ae990-214">Modified</span></span>         | <span data-ttu-id="ae990-215">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="ae990-215">Date last modified</span></span>            | <span data-ttu-id="ae990-216">Представление сведений о стандартной папке</span><span class="sxs-lookup"><span data-stu-id="ae990-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="ae990-217">Создание</span><span class="sxs-lookup"><span data-stu-id="ae990-217">Created</span></span>          | <span data-ttu-id="ae990-218">Дата создания</span><span class="sxs-lookup"><span data-stu-id="ae990-218">Date created</span></span>                  | <span data-ttu-id="ae990-219">Представление сведений о стандартной папке</span><span class="sxs-lookup"><span data-stu-id="ae990-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="ae990-220">Обращения</span><span class="sxs-lookup"><span data-stu-id="ae990-220">Accessed</span></span>         | <span data-ttu-id="ae990-221">Дата последнего доступа</span><span class="sxs-lookup"><span data-stu-id="ae990-221">Date last accessed</span></span>            | <span data-ttu-id="ae990-222">Представление сведений о стандартной папке</span><span class="sxs-lookup"><span data-stu-id="ae990-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="ae990-223">Папка</span><span class="sxs-lookup"><span data-stu-id="ae990-223">InFolder</span></span>         | <span data-ttu-id="ae990-224">Каталог, содержащий файл</span><span class="sxs-lookup"><span data-stu-id="ae990-224">Directory containing the file</span></span> | <span data-ttu-id="ae990-225">Результаты поиска документов</span><span class="sxs-lookup"><span data-stu-id="ae990-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="ae990-226">Ранг</span><span class="sxs-lookup"><span data-stu-id="ae990-226">Rank</span></span>             | <span data-ttu-id="ae990-227">Соответствие качества поиска</span><span class="sxs-lookup"><span data-stu-id="ae990-227">Quality of search match</span></span>       | <span data-ttu-id="ae990-228">Результаты поиска документов</span><span class="sxs-lookup"><span data-stu-id="ae990-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="ae990-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="ae990-229">FreeSpace</span></span>        | <span data-ttu-id="ae990-230">Доступное дисковое пространство</span><span class="sxs-lookup"><span data-stu-id="ae990-230">Available storage space</span></span>       | <span data-ttu-id="ae990-231">Диски</span><span class="sxs-lookup"><span data-stu-id="ae990-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="ae990-232">NumberOfVisits</span><span class="sxs-lookup"><span data-stu-id="ae990-232">NumberOfVisits</span></span>   | <span data-ttu-id="ae990-233">Количество посещений</span><span class="sxs-lookup"><span data-stu-id="ae990-233">Number of visits</span></span>              | <span data-ttu-id="ae990-234">Папка "Избранное"</span><span class="sxs-lookup"><span data-stu-id="ae990-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="ae990-235">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ae990-235">Attributes</span></span>       | <span data-ttu-id="ae990-236">Атрибуты файла</span><span class="sxs-lookup"><span data-stu-id="ae990-236">File Attributes</span></span>               | <span data-ttu-id="ae990-237">Представление сведений о стандартной папке</span><span class="sxs-lookup"><span data-stu-id="ae990-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="ae990-238">Company</span><span class="sxs-lookup"><span data-stu-id="ae990-238">Company</span></span>          | <span data-ttu-id="ae990-239">Название организации</span><span class="sxs-lookup"><span data-stu-id="ae990-239">Company name</span></span>                  | [<span data-ttu-id="ae990-240">**\_компания пиддси**</span><span class="sxs-lookup"><span data-stu-id="ae990-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="ae990-241">Category</span><span class="sxs-lookup"><span data-stu-id="ae990-241">Category</span></span>         | <span data-ttu-id="ae990-242">Категория документа</span><span class="sxs-lookup"><span data-stu-id="ae990-242">Document category</span></span>             | [<span data-ttu-id="ae990-243">**\_Категория пиддси**</span><span class="sxs-lookup"><span data-stu-id="ae990-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="ae990-244">Авторские права</span><span class="sxs-lookup"><span data-stu-id="ae990-244">Copyright</span></span>        | <span data-ttu-id="ae990-245">Авторские права на мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ae990-245">Media copyright</span></span>               | [<span data-ttu-id="ae990-246">**ПИДМСИ \_ авторские права**</span><span class="sxs-lookup"><span data-stu-id="ae990-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="ae990-247">хтмлинфотипфиле</span><span class="sxs-lookup"><span data-stu-id="ae990-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="ae990-248">Файл всплывающей подсказки HTML</span><span class="sxs-lookup"><span data-stu-id="ae990-248">HTML InfoTip file</span></span>             | <span data-ttu-id="ae990-249">Файл Desktop.ini для папки</span><span class="sxs-lookup"><span data-stu-id="ae990-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ae990-250">См. также</span><span class="sxs-lookup"><span data-stu-id="ae990-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae990-251">Регистрация обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="ae990-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 

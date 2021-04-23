---
title: Пример диалогового окна "Открыть"
description: Пример Shapes, который мы использовали, немного надуманный. Давайте перейдем к COM-объекту, который можно использовать в реальной программе Windows в диалоговом окне Открыть.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412927"
---
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="5e36d-104">Пример. диалоговое окно "Открыть"</span><span class="sxs-lookup"><span data-stu-id="5e36d-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="5e36d-105">`Shapes`Пример, который мы использовали, немного надуманный.</span><span class="sxs-lookup"><span data-stu-id="5e36d-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="5e36d-106">Давайте перейдем к COM-объекту, который можно использовать в реальной программе Windows: диалоговое окно **Открыть** .</span><span class="sxs-lookup"><span data-stu-id="5e36d-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![снимок экрана, показывающий диалоговое окно "Открыть"](images/fileopen01.png)

<span data-ttu-id="5e36d-108">Чтобы отобразить диалоговое окно **Открыть** , программа может использовать COM-объект, называемый объектом диалогового окна общих элементов.</span><span class="sxs-lookup"><span data-stu-id="5e36d-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="5e36d-109">В диалоговом окне Общие элементы реализуется интерфейс с именем [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), который объявлен в файле заголовка shobjidl. h.</span><span class="sxs-lookup"><span data-stu-id="5e36d-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="5e36d-110">Ниже приведена программа, которая отображает диалоговое окно **Открыть** для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e36d-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="5e36d-111">Если пользователь выбирает файл, программа отображает диалоговое окно, содержащее имя файла.</span><span class="sxs-lookup"><span data-stu-id="5e36d-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="5e36d-112">В этом коде используются некоторые понятия, которые будут описаны далее в модуле, поэтому не беспокойтесь, если вы не понимаете все здесь.</span><span class="sxs-lookup"><span data-stu-id="5e36d-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="5e36d-113">Ниже приведена базовая структура кода.</span><span class="sxs-lookup"><span data-stu-id="5e36d-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="5e36d-114">Вызов [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="5e36d-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="5e36d-115">Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать объект диалогового окна общих элементов и получить указатель на интерфейс [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) объекта.</span><span class="sxs-lookup"><span data-stu-id="5e36d-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="5e36d-116">Вызовите метод « **Показать** » объекта, который показывает диалоговое окно для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e36d-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="5e36d-117">Этот метод блокируется до тех пор, пока пользователь не закрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5e36d-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="5e36d-118">Вызовите [**метод GetObject объекта.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)</span><span class="sxs-lookup"><span data-stu-id="5e36d-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="5e36d-119">Этот метод возвращает указатель на второй COM-объект, называемый объектом *элемента оболочки* .</span><span class="sxs-lookup"><span data-stu-id="5e36d-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="5e36d-120">Элемент оболочки, реализующий интерфейс [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , представляет файл, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="5e36d-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="5e36d-121">Вызовите метод « [**выводить**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) » элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="5e36d-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="5e36d-122">Этот метод получает путь к файлу в виде строки.</span><span class="sxs-lookup"><span data-stu-id="5e36d-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="5e36d-123">Отображение окна сообщения, в котором отображается путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="5e36d-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="5e36d-124">Вызовите [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) , чтобы отменить инициализацию библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="5e36d-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="5e36d-125">Шаги 1, 2 и 7 вызывают функции, определяемые библиотекой COM.</span><span class="sxs-lookup"><span data-stu-id="5e36d-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="5e36d-126">Это универсальные функции COM.</span><span class="sxs-lookup"><span data-stu-id="5e36d-126">These are generic COM functions.</span></span> <span data-ttu-id="5e36d-127">Шаги 3 – 5 вызывают методы, определяемые объектом диалогового окна общих элементов.</span><span class="sxs-lookup"><span data-stu-id="5e36d-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="5e36d-128">В этом примере показаны оба вида создания объектов: универсальная функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) и метод ([**result**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)), характерный для объекта диалогового окна общих элементов.</span><span class="sxs-lookup"><span data-stu-id="5e36d-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="5e36d-129">Следующая</span><span class="sxs-lookup"><span data-stu-id="5e36d-129">Next</span></span>

[<span data-ttu-id="5e36d-130">Управление жизненным циклом объекта</span><span class="sxs-lookup"><span data-stu-id="5e36d-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="5e36d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5e36d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e36d-132">Открыть образец диалогового окна</span><span class="sxs-lookup"><span data-stu-id="5e36d-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 
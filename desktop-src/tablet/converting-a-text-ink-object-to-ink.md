---
description: Реализация преобразования из объекта рукописного ввода текста (Тинк) в рукописный текст.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Преобразование объекта рукописного ввода текста в рукописный текст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c7fe4a7847834fffda2df9c4ab94293756cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262779"
---
# <a name="converting-a-text-ink-object-to-ink"></a><span data-ttu-id="aee5a-103">Преобразование объекта рукописного ввода текста в рукописный текст</span><span class="sxs-lookup"><span data-stu-id="aee5a-103">Converting a Text Ink Object to Ink</span></span>

<span data-ttu-id="aee5a-104">Реализация преобразования из объекта рукописного ввода текста (Тинк) в рукописный текст.</span><span class="sxs-lookup"><span data-stu-id="aee5a-104">Implementation of converting from a text ink object (tInk) to ink.</span></span>

## <a name="to-convert-from-a-text-ink-object-to-ink"></a><span data-ttu-id="aee5a-105">Преобразование объекта рукописного ввода текста в рукописный ввод</span><span class="sxs-lookup"><span data-stu-id="aee5a-105">To convert from a text ink object to ink</span></span>

1.  <span data-ttu-id="aee5a-106">Используйте интерфейс [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) для записи содержимого объекта рукописного ввода текста в поток.</span><span class="sxs-lookup"><span data-stu-id="aee5a-106">Use the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to write the contents of the text ink object out to a stream.</span></span> <span data-ttu-id="aee5a-107">Объект рукописного ввода текста использует сериализованный формат рукописного ввода для записи в Steam.</span><span class="sxs-lookup"><span data-stu-id="aee5a-107">The text ink object uses ink serialized format to write to the steam.</span></span>
2.  <span data-ttu-id="aee5a-108">Считывает содержимое потока в массив БАЙТОВ.</span><span class="sxs-lookup"><span data-stu-id="aee5a-108">Read the contents of the stream into a BYTE array.</span></span>
3.  <span data-ttu-id="aee5a-109">Используйте метод [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) объекта [**инкдисп**](inkdisp-class.md) , чтобы загрузить содержимое потока в объект **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="aee5a-109">Use the [**InkDisp**](inkdisp-class.md) object's [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) method to load the contents of the stream into the **InkDisp** object.</span></span>

## <a name="text-ink-object-to-ink-object-example"></a><span data-ttu-id="aee5a-110">Пример объекта рукописного ввода текста на рукописный объект</span><span class="sxs-lookup"><span data-stu-id="aee5a-110">Text Ink Object to Ink Object Example</span></span>

<span data-ttu-id="aee5a-111">Следующий фрагмент кода преобразует объект рукописного ввода текста в рукописный текст.</span><span class="sxs-lookup"><span data-stu-id="aee5a-111">The following code fragment converts a text ink object to ink.</span></span>

<span data-ttu-id="aee5a-112">Во-первых, код получает объект рукописного ввода текста.</span><span class="sxs-lookup"><span data-stu-id="aee5a-112">First, the code obtains a text ink object.</span></span>


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



<span data-ttu-id="aee5a-113">Затем код создает указатель для потока, содержащего содержимое объекта рукописного ввода текста.</span><span class="sxs-lookup"><span data-stu-id="aee5a-113">Then, the code creates a pointer for the stream that holds the contents of the text ink object.</span></span>


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



<span data-ttu-id="aee5a-114">Затем код получает интерфейс [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) из объекта рукописного ввода текста.</span><span class="sxs-lookup"><span data-stu-id="aee5a-114">Then, the code obtains the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface from the text ink object.</span></span>


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



<span data-ttu-id="aee5a-115">Затем код использует интерфейс [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) для сохранения содержимого текстового рукописного объекта в поток.</span><span class="sxs-lookup"><span data-stu-id="aee5a-115">Then, the code uses the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to save the contents of the text ink object to the stream.</span></span>


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



<span data-ttu-id="aee5a-116">Затем код создает объект [**InkCollector**](inkcollector-class.md) , создает объект [**Инкдисп**](inkdisp-class.md) для объекта **InkCollector**, присоединяет **InkCollector** к окну приложения и включает сбор рукописных данных для объекта **InkCollector**.</span><span class="sxs-lookup"><span data-stu-id="aee5a-116">Then, the code creates an [**InkCollector**](inkcollector-class.md) object, creates an [**InkDisp**](inkdisp-class.md) object for the **InkCollector**, attaches the **InkCollector** to the application window, and enables ink collection on the **InkCollector**.</span></span>


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



<span data-ttu-id="aee5a-117">Затем код получает размер потока и создает защищенный массив для хранения содержимого потока.</span><span class="sxs-lookup"><span data-stu-id="aee5a-117">Then, the code retrieves the size of the stream and creates a safe array to hold the contents of the stream.</span></span>


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



<span data-ttu-id="aee5a-118">Наконец, код обращается к защищенному массиву и использует метод [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) объекта [**инкдисп**](inkdisp-class.md) для загрузки рукописного ввода из массива.</span><span class="sxs-lookup"><span data-stu-id="aee5a-118">Finally, the code accesses the safe array and uses the [**InkDisp**](inkdisp-class.md) object's [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) method to load the ink from the array.</span></span>


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 

---
title: Примеры распространенных классов
description: Примеры кода в этом разделе можно использовать в качестве отправной точки для многих приложений фоновая интеллектуальная служба передачи (BITS), выполняющих инициализацию COM, требующих обработки ошибок и получения уведомлений обратного вызова.
ms.assetid: 8fe722a3-fbab-4843-b298-1ea11f54d7a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864fe4aa8d7af5bb6a248364b0e2c636e1c250a6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797286"
---
# <a name="example-common-classes"></a><span data-ttu-id="8874a-103">Пример. Общие классы</span><span class="sxs-lookup"><span data-stu-id="8874a-103">Example: Common Classes</span></span>

<span data-ttu-id="8874a-104">Примеры кода в этом разделе можно использовать в качестве отправной точки для многих приложений фоновая интеллектуальная служба передачи (BITS), выполняющих инициализацию COM, требующих обработки ошибок и получения уведомлений обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8874a-104">You can use the code examples in this topic as a starting point for many Background Intelligent Transfer Service (BITS) applications that perform COM initialization, need error handling, and receive callback notifications.</span></span>


<span data-ttu-id="8874a-105">В следующем примере кода определяется класс исключения для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="8874a-105">The following code example defines an exception class to handle errors.</span></span>


```C++
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};
```



<span data-ttu-id="8874a-106">Класс Мексцептион является универсальным классом исключений, который принимает код HRESULT и строку ошибки.</span><span class="sxs-lookup"><span data-stu-id="8874a-106">The MyException class is a generic exception class that accepts an HRESULT code and error string.</span></span>


<span data-ttu-id="8874a-107">В следующем примере кода определяется вспомогательный класс для получения ресурсов для функции [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="8874a-107">The following code example defines a resource acquisition helper class for the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span>


```C++
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};
```



<span data-ttu-id="8874a-108">Класс Ккоинитиализер работает с выделением и освобождением ресурсов для инициализации COM.</span><span class="sxs-lookup"><span data-stu-id="8874a-108">The CCoInitializer class deals with resource allocation and deallocation for COM initialization.</span></span> <span data-ttu-id="8874a-109">Этот класс позволяет вызывать деструктор, когда класс выходит из области действия.</span><span class="sxs-lookup"><span data-stu-id="8874a-109">This class enables the destructor to be called when the class goes out of scope.</span></span> <span data-ttu-id="8874a-110">Этот класс устраняет необходимость вызова метода [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) после каждого блока исключения.</span><span class="sxs-lookup"><span data-stu-id="8874a-110">This class eliminates the need for the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) method to be called after every exception block.</span></span>


<span data-ttu-id="8874a-111">В следующем примере кода показано объявление интерфейса обратного вызова Кнотифинтерфаце.</span><span class="sxs-lookup"><span data-stu-id="8874a-111">The following code example is the declaration of the CNotifyInterface callback interface.</span></span>


```C++
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor
    CNotifyInterface() {m_lRefCount = 1;};

//Destructor
    ~CNotifyInterface() {};

    //IUnknown methods
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);

private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```



<span data-ttu-id="8874a-112">Класс Кнотифинтерфаце, производный от интерфейса [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="8874a-112">The CNotifyInterface class derived from the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span> <span data-ttu-id="8874a-113">Класс Кнотифинтерфаце реализует интерфейс IUnknown.</span><span class="sxs-lookup"><span data-stu-id="8874a-113">The CNotifyInterface class implements the IUnknown interface.</span></span> <span data-ttu-id="8874a-114">Дополнительные сведения см. в разделе [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="8874a-114">For more information, see [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="8874a-115">Кнотифинтерфаце использует следующие методы для получения уведомления о завершении задания, его изменении или в состоянии ошибки: [**жобтрансферред**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**жобмодификатион**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)и [**жоберрор**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror).</span><span class="sxs-lookup"><span data-stu-id="8874a-115">CNotifyInterface uses the following methods to receive notification that a job is complete, has been modified, or is in an error state: [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification), and [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror).</span></span> <span data-ttu-id="8874a-116">Все эти методы принимают объект задания [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .</span><span class="sxs-lookup"><span data-stu-id="8874a-116">All of these methods take an [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) job object.</span></span>

<span data-ttu-id="8874a-117">В этом примере для освобождения ресурсов памяти используется [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .</span><span class="sxs-lookup"><span data-stu-id="8874a-117">This example uses the [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free memory resources.</span></span>


<span data-ttu-id="8874a-118">В следующем примере кода показана реализация интерфейса обратного вызова [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="8874a-118">The following code example is the implementation of the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) callback interface.</span></span>


```C++
HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed. 

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }
    
    // Clean up
    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```




<span data-ttu-id="8874a-119">Следующий файл заголовка используется для общих классов кода.</span><span class="sxs-lookup"><span data-stu-id="8874a-119">The following header file is used for the common code classes.</span></span> <span data-ttu-id="8874a-120">Эти классы используются в предыдущих примерах кода.</span><span class="sxs-lookup"><span data-stu-id="8874a-120">These classes are used in the previous code examples.</span></span>


```C++
// commoncode.h
#pragma once

//
// Exception class used for error handling
//
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};

// CoInitialize helper class
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};

//
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor, Destructor
    CNotifyInterface() {m_lRefCount = 1;};
    ~CNotifyInterface() {};

    //IUnknown
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback2 methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```




<span data-ttu-id="8874a-121">Следующий пример кода является реализацией общих классов кода.</span><span class="sxs-lookup"><span data-stu-id="8874a-121">The following example code is the implementation of the common code classes.</span></span>


```C++
//commoncode.cpp

#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed.

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }

    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="8874a-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8874a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8874a-123">IUnknown</span><span class="sxs-lookup"><span data-stu-id="8874a-123">IUnknown</span></span>]( /windows/win32/api/unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="8874a-124">**ибаккграундкопикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="8874a-124">**IBackgroundCopyCallback**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)
</dt> <dt>

[<span data-ttu-id="8874a-125">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="8874a-125">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="8874a-126">CoInitializeEx</span><span class="sxs-lookup"><span data-stu-id="8874a-126">CoInitializeEx</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="8874a-127">CoUninitialize</span><span class="sxs-lookup"><span data-stu-id="8874a-127">CoUninitialize</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)
</dt> </dl>

 

 
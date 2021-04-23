---
description: Реализация Имедиабуффер
ms.assetid: bde7cef8-f43e-4a11-8b77-fed5585d390a
title: Реализация Имедиабуффер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3425b3f612667a0b6577de385d59362bd8dafd0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674549"
---
# <a name="implementing-imediabuffer"></a><span data-ttu-id="86ff1-103">Реализация Имедиабуффер</span><span class="sxs-lookup"><span data-stu-id="86ff1-103">Implementing IMediaBuffer</span></span>

<span data-ttu-id="86ff1-104">В модели потоковой передачи DMO по умолчанию Управление буферами осуществляется через интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="86ff1-104">In the default DMO streaming model, buffers are managed through the [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="86ff1-105">Клиент DMO отвечает за реализацию объекта, предоставляющего этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="86ff1-105">The client of the DMO is responsible for implementing an object that exposes this interface.</span></span> <span data-ttu-id="86ff1-106">Интерфейс **имедиабуффер** имеет три метода:</span><span class="sxs-lookup"><span data-stu-id="86ff1-106">The **IMediaBuffer** interface has three methods:</span></span>

-   <span data-ttu-id="86ff1-107">**Жетбуфферандленгс** возвращает адрес буфера (то есть реальный блок памяти, в котором хранятся данные) и размер всех допустимых данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="86ff1-107">**GetBufferAndLength** returns the address of the buffer (that is, the actual block of memory that holds the data) and the size of any valid data in the buffer.</span></span>
-   <span data-ttu-id="86ff1-108">Функция **MaxLength** возвращает размер буфера.</span><span class="sxs-lookup"><span data-stu-id="86ff1-108">**GetMaxLength** returns the size of the buffer.</span></span>
-   <span data-ttu-id="86ff1-109">**SetLength** указывает длину допустимых данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="86ff1-109">**SetLength** specifies the length of the valid data in the buffer.</span></span>

<span data-ttu-id="86ff1-110">Для обработки на месте интерфейс **имедиабуффер** не требуется.</span><span class="sxs-lookup"><span data-stu-id="86ff1-110">In-place processing does not require the **IMediaBuffer** interface.</span></span> <span data-ttu-id="86ff1-111">В следующем коде показана минимальная реализация **имедиабуффер**:</span><span class="sxs-lookup"><span data-stu-id="86ff1-111">The following code shows a minimal implementation of **IMediaBuffer**:</span></span>


```C++
//  CMediaBuffer class.
#include <dmo.h>
class CMediaBuffer : public IMediaBuffer
{
private:
    DWORD        m_cbLength;
    const DWORD  m_cbMaxLength;
    LONG         m_nRefCount;  // Reference count
    BYTE         *m_pbData;


    CMediaBuffer(DWORD cbMaxLength, HRESULT& hr) :
        m_nRefCount(1),
        m_cbMaxLength(cbMaxLength),
        m_cbLength(0),
        m_pbData(NULL)
    {
        m_pbData = new BYTE[cbMaxLength];
        if (!m_pbData) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    ~CMediaBuffer()
    {
        if (m_pbData) 
        {
            delete [] m_pbData;
        }
    }

public:

    // Function to create a new IMediaBuffer object and return 
    // an AddRef'd interface pointer.
    static HRESULT Create(long cbMaxLen, IMediaBuffer **ppBuffer)
    {
        HRESULT hr = S_OK;
        CMediaBuffer *pBuffer = NULL;

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }

        pBuffer = new CMediaBuffer(cbMaxLen, hr);

        if (pBuffer == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
           *ppBuffer = pBuffer;
           (*ppBuffer)->AddRef();
        }

        if (pBuffer)
        {
            pBuffer->Release();
        }
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        if (ppv == NULL) 
        {
            return E_POINTER;
        }
        else if (riid == IID_IMediaBuffer || riid == IID_IUnknown) 
        {
            *ppv = static_cast<IMediaBuffer *>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRef = InterlockedDecrement(&m_nRefCount);
        if (lRef == 0) 
        {
            delete this;
            // m_cRef is no longer valid! Return lRef.
        }
        return lRef;  
    }

    // IMediaBuffer methods.
    STDMETHODIMP SetLength(DWORD cbLength)
    {
        if (cbLength > m_cbMaxLength) 
        {
            return E_INVALIDARG;
        }
        m_cbLength = cbLength;
        return S_OK;
    }

    STDMETHODIMP GetMaxLength(DWORD *pcbMaxLength)
    {
        if (pcbMaxLength == NULL) 
        {
            return E_POINTER;
        }
        *pcbMaxLength = m_cbMaxLength;
        return S_OK;
    }

    STDMETHODIMP GetBufferAndLength(BYTE **ppbBuffer, DWORD *pcbLength)
    {
        // Either parameter can be NULL, but not both.
        if (ppbBuffer == NULL && pcbLength == NULL) 
        {
            return E_POINTER;
        }
        if (ppbBuffer) 
        {
            *ppbBuffer = m_pbData;
        }
        if (pcbLength) 
        {
            *pcbLength = m_cbLength;
        }
        return S_OK;
    }
};

```



## <a name="related-topics"></a><span data-ttu-id="86ff1-112">См. также</span><span class="sxs-lookup"><span data-stu-id="86ff1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ff1-113">Непосредственное размещение DMO</span><span class="sxs-lookup"><span data-stu-id="86ff1-113">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 




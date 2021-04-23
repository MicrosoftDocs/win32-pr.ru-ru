---
description: Управление сертификатами, созданным на языке C++
ms.assetid: 19dd2fce-b4a9-44fd-9572-897ee7943914
title: Управление сертификатами, созданным на языке C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 868f89e0a285460c587a924e84a5ed21c202eb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818977"
---
# <a name="the-certificate-enrollment-control-instantiated-in-c"></a><span data-ttu-id="a3339-103">Управление сертификатами, созданным на языке C++</span><span class="sxs-lookup"><span data-stu-id="a3339-103">The Certificate Enrollment Control Instantiated in C++</span></span>

<span data-ttu-id="a3339-104">В следующем примере кода C++ инициализируется COM, создается экземпляр [управления регистрацией сертификатов](certificate-enrollment-control.md), используется Управление регистрацией сертификатов и освобождаются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a3339-104">The following C++ example initializes COM, creates an instance of the [Certificate Enrollment Control](certificate-enrollment-control.md), uses the Certificate Enrollment Control, and frees resources.</span></span>

## <a name="example-in-c"></a><span data-ttu-id="a3339-105">Пример в C++</span><span class="sxs-lookup"><span data-stu-id="a3339-105">Example in C++</span></span>

<span data-ttu-id="a3339-106">В следующем примере создается экземпляр [управления регистрацией сертификата](certificate-enrollment-control.md) и отображается значение свойства [**мисторенаме**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .</span><span class="sxs-lookup"><span data-stu-id="a3339-106">The following example creates an instance of the [Certificate Enrollment Control](certificate-enrollment-control.md) and displays the value of the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span> <span data-ttu-id="a3339-107">В этом примере используется интерфейс [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) .</span><span class="sxs-lookup"><span data-stu-id="a3339-107">This example uses the [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) interface.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <xenroll.h>

// Copyright (C) Microsoft.  All rights reserved.
HRESULT __cdecl main(void)
{
    HRESULT hr = 0;
    ICEnroll4 *pEnroll = NULL;
    BSTR bstrStoreName = NULL;

    // Initialize COM.
    hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
    if ( FAILED( hr ) )
    {
        printf("Failed CoInitializeEx - [0x%x]\n", hr);
        exit(hr);
    }

    // Create an instance of the object.
    hr = CoCreateInstance( __uuidof(CEnroll),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(ICEnroll4),
                           (void **)&pEnroll);
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pEnroll [0x%x]\n", hr);
        exit(hr);
    }

    hr = pEnroll->get_MyStoreName(&bstrStoreName);
    if (SUCCEEDED(hr))
    {
        printf("The value of MyStoreName is %ws\n", bstrStoreName);
    }
    else
    {
        printf("pEnroll->GetMyStoreName failed: 0x%x\n", hr);
    }

    pEnroll->Release();
    SysFreeString(bstrStoreName);
    CoUninitialize();

    return hr;
}
```



 

 

---
description: Следующая процедура содержит краткий обзор процесса сборки.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Создание команды КАТЕГОРИЯХ APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263471"
---
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="6436f-103">Создание команды КАТЕГОРИЯХ APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="6436f-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="6436f-104">Чтобы добавить функциональные возможности для поставщика услуг, необходимо знать, как будет создаваться [*блок данных протокола приложения*](/windows/desktop/SecGloss/a-gly) ISO7816-4 (категориях APDU) в базовых библиотеках DLL поставщика служб.</span><span class="sxs-lookup"><span data-stu-id="6436f-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="6436f-105">Следующая процедура содержит краткий обзор процесса сборки.</span><span class="sxs-lookup"><span data-stu-id="6436f-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="6436f-106">Представленный здесь пример не обязательно должен быть полным. Дополнительные сведения см. в примерах приложений и библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="6436f-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="6436f-107">**Создание команды ISO7816-4 КАТЕГОРИЯХ APDU**</span><span class="sxs-lookup"><span data-stu-id="6436f-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="6436f-108">Создайте объект [**искардкмд**](iscardcmd.md) и объект [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="6436f-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    <span data-ttu-id="6436f-109">Интерфейс [**искардкмд**](iscardcmd.md) содержит два буфера **ибитебуффер** .</span><span class="sxs-lookup"><span data-stu-id="6436f-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="6436f-110">Один буфер содержит собственно командную строку КАТЕГОРИЯХ APDU (а также любые данные для отправки с помощью команды).</span><span class="sxs-lookup"><span data-stu-id="6436f-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="6436f-111">Другой содержит все сведения ответа, возвращаемые картой после выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="6436f-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="6436f-112">Используя эти объекты, создайте допустимую команду ISO7816-4 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6436f-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="6436f-113">Ниже приведен [**код, используемый в методе**](iscardiso7816-getchallenge.md) метода WebMethod:</span><span class="sxs-lookup"><span data-stu-id="6436f-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    <span data-ttu-id="6436f-114">Метод [**ISCardISO7816:: unchallenge**](iscardiso7816-getchallenge.md) использует метод [**Искардкмд:: буилдкмд**](iscardcmd-buildcmd.md) для создания запрошенного категориях APDU.</span><span class="sxs-lookup"><span data-stu-id="6436f-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="6436f-115">Это делается путем записи соответствующей информации в буфер категориях APDU [**искардкмд**](iscardcmd.md) в следующей инструкции:</span><span class="sxs-lookup"><span data-stu-id="6436f-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="6436f-116">С помощью созданного объекта [**искардкмд**](iscardcmd.md) выполните транзакцию с картой, воспримете результаты и продолжайте.</span><span class="sxs-lookup"><span data-stu-id="6436f-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="6436f-117">Расширение за пределами ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="6436f-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="6436f-118">Чтобы расширить процесс сборки или выполнения поставщика услуг, описанный выше, рекомендуется создать новый COM-объект.</span><span class="sxs-lookup"><span data-stu-id="6436f-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="6436f-119">Этот COM-объект должен поддерживать новый интерфейс, который позволяет создавать команды, отличные от ISO7816-4, и выполнять статистическую обработку интерфейса [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="6436f-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="6436f-120">Пример создания команды КАТЕГОРИЯХ APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="6436f-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="6436f-121">В следующем примере показан код, используемый в процедуре выше.</span><span class="sxs-lookup"><span data-stu-id="6436f-121">The following example shows the code used in the procedure above.</span></span>


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 

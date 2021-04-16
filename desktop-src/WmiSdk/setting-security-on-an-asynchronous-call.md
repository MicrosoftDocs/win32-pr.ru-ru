---
description: Асинхронные вызовы представляют серьезную угрозу безопасности, так как обратный вызов приемника может не быть результатом асинхронного вызова исходного приложения или сценария.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Настройка безопасности при асинхронном вызове
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712948"
---
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="a10ce-103">Настройка безопасности при асинхронном вызове</span><span class="sxs-lookup"><span data-stu-id="a10ce-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="a10ce-104">Асинхронные вызовы представляют серьезную угрозу безопасности, так как обратный вызов [*приемника*](gloss-s.md) может не быть результатом асинхронного вызова исходного приложения или сценария.</span><span class="sxs-lookup"><span data-stu-id="a10ce-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="a10ce-105">Безопасность в удаленных подключениях основана на шифровании взаимодействия между клиентом и поставщиком на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a10ce-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="a10ce-106">В C++ можно задать шифрование с помощью параметра уровня проверки подлинности в вызове [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="a10ce-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a10ce-107">В скриптах задайте *аусентикатионлевел* в соединении моникера или в объекте [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="a10ce-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="a10ce-108">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a10ce-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="a10ce-109">Существуют угрозы безопасности для асинхронных вызовов, так как WMI понижает уровень проверки подлинности обратного вызова до тех пор, пока обратный вызов не завершится.</span><span class="sxs-lookup"><span data-stu-id="a10ce-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="a10ce-110">При исходящем асинхронном вызове клиент может задать уровень проверки подлинности для соединения с WMI.</span><span class="sxs-lookup"><span data-stu-id="a10ce-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="a10ce-111">Инструментарий WMI извлекает параметры безопасности в клиентском вызове и пытается выполнить обратный вызов с тем же уровнем проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a10ce-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="a10ce-112">Обратный вызов всегда инициируется на уровне **\_ конфиденциальности " \_ \_ \_ PKT \_ " RPC C AUTHN** .</span><span class="sxs-lookup"><span data-stu-id="a10ce-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="a10ce-113">В случае сбоя обратного вызова Инструментарий WMI понижает уровень проверки подлинности до уровня, в котором обратный вызов может быть успешным, если это необходимо, на **\_ уровень RPC C \_ AUTHN \_ Level \_ None**.</span><span class="sxs-lookup"><span data-stu-id="a10ce-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="a10ce-114">В контексте вызовов в локальной системе, где служба проверки подлинности не является протоколом Kerberos, обратный вызов всегда возвращается **на \_ уровне RPC C \_ AUTHN \_ уровня \_ None**.</span><span class="sxs-lookup"><span data-stu-id="a10ce-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="a10ce-115">Минимальный уровень проверки подлинности — **RPC \_ C \_ AUTHN \_ Level \_ PKT** (**вбемаусентикатионлевелпкт** для сценариев).</span><span class="sxs-lookup"><span data-stu-id="a10ce-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="a10ce-116">Однако вы можете указать более высокий уровень, например **RPC \_ C \_ AUTHN \_ Level \_ PKT \_** (**вбемаусентикатионлевелпктприваци**).</span><span class="sxs-lookup"><span data-stu-id="a10ce-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="a10ce-117">Рекомендуется, чтобы клиентские приложения или скрипты установили уровень проверки подлинности **RPC \_ C \_ AUTHN \_ уровня \_ по умолчанию** (**вбемаусентикатионлевелдефаулт**), что позволяет согласовать уровень проверки подлинности с уровнем, указанным сервером.</span><span class="sxs-lookup"><span data-stu-id="a10ce-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="a10ce-118">Значение реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **унсекаппакцессконтролдефаулт** определяет, будет ли Инструментарий WMI проверять наличие приемлемого уровня проверки подлинности в ответных вызовах.</span><span class="sxs-lookup"><span data-stu-id="a10ce-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="a10ce-119">Это единственный механизм защиты приемника для асинхронных вызовов, выполняемых в сценариях или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a10ce-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="a10ce-120">По умолчанию этот раздел реестра имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="a10ce-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="a10ce-121">Если раздел реестра равен нулю, Инструментарий WMI не проверяет уровни проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a10ce-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="a10ce-122">Чтобы защитить асинхронные вызовы в скриптах, установите для раздела реестра значение 1.</span><span class="sxs-lookup"><span data-stu-id="a10ce-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="a10ce-123">Клиенты C++ могут вызывать [**ивбемунсекуредапартмент:: креатесинкстуб**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) для управления доступом к приемнику.</span><span class="sxs-lookup"><span data-stu-id="a10ce-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="a10ce-124">Значение по умолчанию создается в любой точке.</span><span class="sxs-lookup"><span data-stu-id="a10ce-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="a10ce-125">В следующих разделах приводятся примеры настройки безопасности асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="a10ce-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="a10ce-126">Настройка безопасности при асинхронном вызове в VBScript</span><span class="sxs-lookup"><span data-stu-id="a10ce-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="a10ce-127">Настройка безопасности асинхронных вызовов в C++</span><span class="sxs-lookup"><span data-stu-id="a10ce-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="a10ce-128">Настройка безопасности асинхронных вызовов в C++</span><span class="sxs-lookup"><span data-stu-id="a10ce-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="a10ce-129">Метод [**ивбемунсекуредапартмент:: креатесинкстуб**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) аналогичен методу [**Иунсекуредапартмент:: креатеобжектстуб**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) и создает приемник в отдельном процессе, Unsecapp.exe для получения обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="a10ce-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="a10ce-130">Однако метод **креатесинкстуб** имеет параметр *dwFlag*, который определяет, как отдельный процесс обрабатывает управление доступом.</span><span class="sxs-lookup"><span data-stu-id="a10ce-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="a10ce-131">Параметр *dwFlag* задает одно из следующих действий для Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="a10ce-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="a10ce-132">Используйте параметр раздела реестра, чтобы определить, следует ли проверять доступ.</span><span class="sxs-lookup"><span data-stu-id="a10ce-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="a10ce-133">Проигнорируйте раздел реестра и всегда проверяйте доступ.</span><span class="sxs-lookup"><span data-stu-id="a10ce-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="a10ce-134">Проигнорируйте раздел реестра и не проверяйте доступ.</span><span class="sxs-lookup"><span data-stu-id="a10ce-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="a10ce-135">В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.</span><span class="sxs-lookup"><span data-stu-id="a10ce-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="a10ce-136">В следующей процедуре описывается выполнение асинхронного вызова с помощью [**ивбемунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="a10ce-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="a10ce-137">**Выполнение асинхронного вызова с помощью Ивбемунсекуредапартмент**</span><span class="sxs-lookup"><span data-stu-id="a10ce-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="a10ce-138">Создайте выделенный процесс с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="a10ce-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="a10ce-139">В следующем примере кода метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) вызывается для создания выделенного процесса.</span><span class="sxs-lookup"><span data-stu-id="a10ce-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="a10ce-140">Создайте экземпляр объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="a10ce-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="a10ce-141">В следующем примере кода создается новый объект приемника.</span><span class="sxs-lookup"><span data-stu-id="a10ce-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="a10ce-142">Создайте заглушку для приемника.</span><span class="sxs-lookup"><span data-stu-id="a10ce-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="a10ce-143">Заглушка — это функция-оболочка, созданная из приемника.</span><span class="sxs-lookup"><span data-stu-id="a10ce-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="a10ce-144">В следующем примере кода создается заглушка для приемника.</span><span class="sxs-lookup"><span data-stu-id="a10ce-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="a10ce-145">Освободите указатель объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="a10ce-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="a10ce-146">Можно освободить указатель на объект, так как заглушка теперь является владельцем указателя.</span><span class="sxs-lookup"><span data-stu-id="a10ce-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="a10ce-147">В следующем примере кода освобождается указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="a10ce-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="a10ce-148">Используйте заглушку при любом асинхронном вызове.</span><span class="sxs-lookup"><span data-stu-id="a10ce-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="a10ce-149">По завершении работы с вызовом Освободите локальный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="a10ce-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="a10ce-150">В следующем примере кода заглушка используется в асинхронном вызове.</span><span class="sxs-lookup"><span data-stu-id="a10ce-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="a10ce-151">Иногда может потребоваться отменить асинхронный вызов после выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="a10ce-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="a10ce-152">Если необходимо отменить вызов, отмените вызов с тем же указателем, который был изначально выполнил вызов.</span><span class="sxs-lookup"><span data-stu-id="a10ce-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="a10ce-153">В следующем примере кода показано, как отменить асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="a10ce-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="a10ce-154">При завершении использования асинхронного вызова Освободите локальный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="a10ce-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="a10ce-155">Не забудьте освободить указатель *пстубсинк* только после того, как вы подтвердите, что асинхронный вызов не должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="a10ce-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="a10ce-156">Кроме того, не освобождайте *пстубсинк* после того, как инструментарий WMI освобождает указатель приемника *псинк* .</span><span class="sxs-lookup"><span data-stu-id="a10ce-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="a10ce-157">При освобождении *пстубсинк* после *псинк* создается циклическая ссылка, в которой приемник и заглушка постоянно остаются в памяти.</span><span class="sxs-lookup"><span data-stu-id="a10ce-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="a10ce-158">Вместо этого можно освободить указатель в вызове [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , СДЕЛАНном WMI, чтобы сообщить о завершении исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="a10ce-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="a10ce-159">После завершения выполните деинициализацию COM с помощью вызова метода [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="a10ce-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="a10ce-160">В следующем примере кода показано, как вызвать метод [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателя *пунсекапп* .</span><span class="sxs-lookup"><span data-stu-id="a10ce-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="a10ce-161">Дополнительные сведения о функции и параметрах [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) см. в документации по [com](../cossdk/component-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a10ce-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 

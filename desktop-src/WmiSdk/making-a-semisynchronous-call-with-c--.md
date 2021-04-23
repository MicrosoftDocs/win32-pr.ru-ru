---
description: 'Вызовы семисинчронаус являются рекомендуемыми средствами для вызова методов WMI, таких как IWbemServices:: ExecMethod и методы поставщика, например метода chkdsk \_ класса Win32 LogicalDisk.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Вызов Семисинчронаус с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546178"
---
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="aceec-103">Вызов Семисинчронаус с помощью C++</span><span class="sxs-lookup"><span data-stu-id="aceec-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="aceec-104">Вызовы семисинчронаус являются рекомендуемыми средствами для вызова методов WMI, таких как [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) и методы поставщика, например [**метода chkdsk \_ класса Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="aceec-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="aceec-105">Одной из недостатков синхронной обработки является то, что вызывающий поток блокируется до завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="aceec-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="aceec-106">Блокирование может вызвать задержку во время обработки.</span><span class="sxs-lookup"><span data-stu-id="aceec-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="aceec-107">В отличие от этого, асинхронный вызов должен реализовывать [**свбемсинк**](swbemsink.md) в скрипте.</span><span class="sxs-lookup"><span data-stu-id="aceec-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="aceec-108">В C++ асинхронный код должен реализовывать интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) , использовать несколько потоков и управлять потоком информации обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="aceec-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="aceec-109">Например, большие результирующие наборы из запросов могут потребовать значительного времени для доставки и принудительного выполнения вызывающей стороны значительных системных ресурсов для выполнения доставки.</span><span class="sxs-lookup"><span data-stu-id="aceec-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="aceec-110">Семисинчронаус обработка позволяет разрешать проблемы с блокированием потока и неуправляемой доставкой, опрашивая Специальный объект состояния, реализующий интерфейс [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .</span><span class="sxs-lookup"><span data-stu-id="aceec-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="aceec-111">С помощью **ивбемкаллресулт** можно повысить скорость и эффективность запросов, перечислений и уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="aceec-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="aceec-112">Следующая процедура описывает, как выполнить вызов семисинчронаус с помощью интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="aceec-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="aceec-113">**Вызов семисинчронаус с помощью интерфейса IWbemServices**</span><span class="sxs-lookup"><span data-stu-id="aceec-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="aceec-114">Сделайте вызов обычным, но с флагом WBEM в параметре *ифлагс* установлен флаг **\_ \_ \_ немедленной** установки.</span><span class="sxs-lookup"><span data-stu-id="aceec-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="aceec-115">**Флаг WBEM можно использовать \_ \_ \_ сразу же** , с другими флагами, допустимыми для конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="aceec-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="aceec-116">Например, для всех вызовов, возвращающих перечислители, следует использовать флаг **WBEM \_ \_ \_ только вперед** .</span><span class="sxs-lookup"><span data-stu-id="aceec-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="aceec-117">Установка этих флагов в сочетании экономит время и пространство и повышает скорость реагирования.</span><span class="sxs-lookup"><span data-stu-id="aceec-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="aceec-118">Опрос результатов.</span><span class="sxs-lookup"><span data-stu-id="aceec-118">Poll for your results.</span></span>

    <span data-ttu-id="aceec-119">При вызове метода, возвращающего перечислитель, например [**IWbemServices:: креатеклассенум**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) или [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), можно опрашивать перечислители с помощью методов [**Иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) или [**иенумвбемклассобжект:: некстасинк**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) .</span><span class="sxs-lookup"><span data-stu-id="aceec-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="aceec-120">Вызов **иенумвбемклассобжект:: некстасинк** не блокируется и возвращается немедленно.</span><span class="sxs-lookup"><span data-stu-id="aceec-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="aceec-121">В фоновом режиме Инструментарий WMI начинает доставлять запрошенное число объектов путем вызова [**ивбемобжектсинк:: обозначают**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="aceec-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="aceec-122">Затем WMI останавливается и ожидает другого вызова **некстасинк** .</span><span class="sxs-lookup"><span data-stu-id="aceec-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="aceec-123">При вызове метода, который не возвращает перечислитель, например [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), необходимо задать для параметра *ппкаллресулт* допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="aceec-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="aceec-124">Используйте [**ивбемкаллресулт:: жеткаллстатус**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) в возвращенном указателе, чтобы **получить \_ WBEM \_ без \_ ошибок**.</span><span class="sxs-lookup"><span data-stu-id="aceec-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="aceec-125">Завершите звонок.</span><span class="sxs-lookup"><span data-stu-id="aceec-125">Finish your call.</span></span>

    <span data-ttu-id="aceec-126">Для вызова, возвращающего перечислитель, WMI вызывает [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , чтобы сообщить о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="aceec-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="aceec-127">Если не требуется весь результат, выпустите перечислитель, вызвав метод [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="aceec-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="aceec-128">Вызов результатов **выпуска** в WMI отменяет доставку всех оставшихся объектов.</span><span class="sxs-lookup"><span data-stu-id="aceec-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="aceec-129">Для вызова, который не использует перечислитель, извлеките объект [**жеткаллстатус**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) через параметр *плстатус* метода.</span><span class="sxs-lookup"><span data-stu-id="aceec-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="aceec-130">В примере кода C++ в этом разделе \# для правильной компиляции требуются следующие операторы include.</span><span class="sxs-lookup"><span data-stu-id="aceec-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="aceec-131">В следующем примере кода показано, как выполнить вызов семисинчронаус для [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="aceec-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a><span data-ttu-id="aceec-132">См. также</span><span class="sxs-lookup"><span data-stu-id="aceec-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aceec-133">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="aceec-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 

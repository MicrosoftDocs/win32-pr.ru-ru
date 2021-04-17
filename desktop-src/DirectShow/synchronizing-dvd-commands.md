---
description: Синхронизация команд DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Синхронизация команд DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674318"
---
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="fd300-103">Синхронизация команд DVD</span><span class="sxs-lookup"><span data-stu-id="fd300-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="fd300-104">Команды DVD не всегда выполняются мгновенно.</span><span class="sxs-lookup"><span data-stu-id="fd300-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="fd300-105">По этой причине некоторые методы в [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="fd300-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="fd300-106">К ним относятся методы воспроизведения, такие как **плайтитле**, и методы навигации по меню, такие как **шовмену** и **ретурнфромсубмену**.</span><span class="sxs-lookup"><span data-stu-id="fd300-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="fd300-107">Асинхронный метод возвращает значение немедленно, не дожидаясь завершения команды.</span><span class="sxs-lookup"><span data-stu-id="fd300-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="fd300-108">После возврата метода другие события могут препятствовать завершению выполнения команды, даже если метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="fd300-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="fd300-109">DirectShow предоставляет несколько вариантов синхронизации команд, от отсутствия синхронизации до полной синхронизации с помощью событий фильтра графа.</span><span class="sxs-lookup"><span data-stu-id="fd300-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="fd300-110">Все асинхронные методы имеют параметр *dwFlags* и параметр *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="fd300-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="fd300-111">Параметр *dwFlags* задает поведение синхронизации, а параметр *ппкмд* возвращает указатель на необязательный объект синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd300-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="fd300-112">Различные варианты поведения в зависимости от значений, которые вы предоставляете для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="fd300-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="fd300-113">**Без синхронизации**</span><span class="sxs-lookup"><span data-stu-id="fd300-113">**No Synchronization**</span></span>

<span data-ttu-id="fd300-114">Для простого приложения для воспроизведения DVD лучшим вариантом может быть просто пропустить проблемы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd300-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="fd300-115">Иногда команда может завершиться ошибкой или при обновлении пользовательский интерфейс может немного отставать, но эти ошибки будут находиться в порядке долей секунд.</span><span class="sxs-lookup"><span data-stu-id="fd300-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="fd300-116">Чтобы выдать команду без синхронизации, установите \_ \_ флаг флага DVD-метки " \_ нет" в параметре *dwFlags* и присвойте параметру *ппкмд* **значение NULL**:</span><span class="sxs-lookup"><span data-stu-id="fd300-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="fd300-117">**Блокировка**</span><span class="sxs-lookup"><span data-stu-id="fd300-117">**Blocking**</span></span>

<span data-ttu-id="fd300-118">Если установить \_ \_ \_ флаг блокировки флага блока DVD-диска EC \_ в параметре *dwFlags* , метод блокируется до завершения команды:</span><span class="sxs-lookup"><span data-stu-id="fd300-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="fd300-119">Фактически этот флаг превращает асинхронный метод в синхронный метод.</span><span class="sxs-lookup"><span data-stu-id="fd300-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="fd300-120">Недостаток заключается в том, что пользовательский интерфейс блокируется при вызове метода из потока приложения.</span><span class="sxs-lookup"><span data-stu-id="fd300-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="fd300-121">**Объект синхронизации**</span><span class="sxs-lookup"><span data-stu-id="fd300-121">**Synchronization Object**</span></span>

<span data-ttu-id="fd300-122">Все асинхронные методы могут возвращать объект синхронизации, который можно использовать для ожидания запуска или завершения команды.</span><span class="sxs-lookup"><span data-stu-id="fd300-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="fd300-123">Чтобы получить этот объект, передайте адрес указателя [**идвдкмд**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) в параметре *ппкмд* :</span><span class="sxs-lookup"><span data-stu-id="fd300-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="fd300-124">Если метод завершается с ошибкой, возвращается новый объект **идвдкмд** .</span><span class="sxs-lookup"><span data-stu-id="fd300-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="fd300-125">Метод [**идвдкмд:: ваитфорстарт**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) блокируется до начала команды, а метод [**Идвдкмд:: ваитфоренд**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) блокируется до завершения команды.</span><span class="sxs-lookup"><span data-stu-id="fd300-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="fd300-126">Возвращаемое значение указывает состояние команды.</span><span class="sxs-lookup"><span data-stu-id="fd300-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="fd300-127">Следующий код функционально эквивалентен установке \_ \_ \_ флага блока флага DVD-диска EC \_ , показанного ранее.</span><span class="sxs-lookup"><span data-stu-id="fd300-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



<span data-ttu-id="fd300-128">В этом случае метод **плайтитле** не блокируется, но приложение блокируется путем вызова **ваитфоренд**.</span><span class="sxs-lookup"><span data-stu-id="fd300-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="fd300-129">**События состояния команды**</span><span class="sxs-lookup"><span data-stu-id="fd300-129">**Command Status Events**</span></span>

<span data-ttu-id="fd300-130">Если установить флаг \_ \_ \_ SendEvents в параметре *DWFLAGS* , то Навигатор DVD отправляет событие [**\_ \_ \_ запуска CMD DVD**](ec-dvd-cmd-start.md) , когда команда начинается, а в случае завершения команды — [**\_ DVD-диску \_ \_ EC**](ec-dvd-cmd-end.md) .</span><span class="sxs-lookup"><span data-stu-id="fd300-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="fd300-131">Параметр *lParam2* события возвращает возвращаемое значение HRESULT для команды.</span><span class="sxs-lookup"><span data-stu-id="fd300-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="fd300-132">Параметр *lParam1* события обеспечивает способ получения объекта синхронизации для команды.</span><span class="sxs-lookup"><span data-stu-id="fd300-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="fd300-133">При передаче *lParam1* в метод [**IDvdInfo2:: жеткмдфромевент**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) метод возвращает указатель на интерфейс **идвдкмд** объекта синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd300-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="fd300-134">Этот интерфейс можно использовать для ожидания завершения команды, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="fd300-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="fd300-135">Однако если в исходном методе **IDvdControl2** передано **значение NULL** для параметра *ппкмд* , то Навигатор DVD не создает объект синхронизации, а **жеткмдфромевент** возвращает \_ ошибку E.</span><span class="sxs-lookup"><span data-stu-id="fd300-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="fd300-136">В следующем коде показано, как использовать события состояния команды без объекта синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd300-136">The following code shows how to use command status events with no synchronization object.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



<span data-ttu-id="fd300-137">Обратите внимание, что без объекта синхронизации невозможно определить, какая команда связана с этим событием.</span><span class="sxs-lookup"><span data-stu-id="fd300-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="fd300-138">В следующем коде показано, как использовать события с объектом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd300-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="fd300-139">Идея состоит в том, чтобы сохранить объекты синхронизации в списке, а затем сравнить указатели объектов при получении события « [**\_ \_ \_ Запуск DVD cmd**](ec-dvd-cmd-start.md) » или « [**EC \_ DVD \_ cmd \_ End**](ec-dvd-cmd-end.md) ».</span><span class="sxs-lookup"><span data-stu-id="fd300-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



<span data-ttu-id="fd300-140">**Сброс буферов для навигатора DVD**</span><span class="sxs-lookup"><span data-stu-id="fd300-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="fd300-141">Во время воспроизведения Навигатор DVD замещает данные видео.</span><span class="sxs-lookup"><span data-stu-id="fd300-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="fd300-142">Количество буферизованных данных различается.</span><span class="sxs-lookup"><span data-stu-id="fd300-142">The amount of buffered data varies.</span></span> <span data-ttu-id="fd300-143">Когда Навигатор DVD переключается на новый фрагмент видео, данные, уже находящийся в конвейере, не теряются, поэтому переход выполняется беспрепятственно.</span><span class="sxs-lookup"><span data-stu-id="fd300-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="fd300-144">По умолчанию, когда DVD-навигатор выдает команду, он не очищает данные, которые уже находятся в конвейере.</span><span class="sxs-lookup"><span data-stu-id="fd300-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="fd300-145">В результате может возникнуть задержка, прежде чем можно будет увидеть результат выполнения команды в зависимости от объема буферизованных данных.</span><span class="sxs-lookup"><span data-stu-id="fd300-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="fd300-146">Чтобы повысить скорость реагирования, можно принудительно сбросить DVD-навигатор, установив \_ \_ флаг сброса флага DVD-диска \_ .</span><span class="sxs-lookup"><span data-stu-id="fd300-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="fd300-147">Этот флаг можно сочетать с любыми указанными выше флагами с помощью побитового или.</span><span class="sxs-lookup"><span data-stu-id="fd300-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="fd300-148">Побочным результатом очистки является то, что некоторое видео может быть потеряно, поэтому не используйте этот флаг, если необходимо гарантировать, что в видео нет пробелов.</span><span class="sxs-lookup"><span data-stu-id="fd300-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd300-149">См. также</span><span class="sxs-lookup"><span data-stu-id="fd300-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd300-150">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="fd300-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




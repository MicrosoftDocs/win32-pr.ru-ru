---
title: Использование пользовательских приемников
description: Использование пользовательских приемников
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Расширенный формат систем (ASF), пользовательские приемники
- ASF (Расширенный системный формат), пользовательские приемники
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, пользовательские приемники
- Пользовательские приемники, сведения
- Приемники модуля записи, пользовательские приемники
- Пользовательские приемники, интерфейс Ивмвритерсинк
- ивмвритерсинк
- Приемники модуля записи, интерфейс Ивмвритерсинк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788749"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="18e5f-113">Использование пользовательских приемников</span><span class="sxs-lookup"><span data-stu-id="18e5f-113">Using Custom Sinks</span></span>

<span data-ttu-id="18e5f-114">Если у вас есть особая потребность в написании, можно создать собственные приемники записи.</span><span class="sxs-lookup"><span data-stu-id="18e5f-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="18e5f-115">Модуль записи поддерживает одностороннее взаимодействие с приемником, выполнив вызовы методов [**ивмвритерсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span><span class="sxs-lookup"><span data-stu-id="18e5f-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="18e5f-116">Чтобы создать собственный приемник, реализуйте интерфейс **ивмвритерсинк** в классе приложения.</span><span class="sxs-lookup"><span data-stu-id="18e5f-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="18e5f-117">Этот процесс очень похож на реализацию любого другого интерфейса обратного вызова, используемого объектами пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="18e5f-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="18e5f-118">Дополнительные сведения о обратных вызовах см. [в разделе Использование методов обратного вызова](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="18e5f-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="18e5f-119">Буфер, полученный в [**ивмвритерсинк:: onhead**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) , должен быть записан в начало файла, и все буферы, полученные в [**ондатаунит**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) , должны быть записаны последовательно.</span><span class="sxs-lookup"><span data-stu-id="18e5f-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="18e5f-120">**Верхний** колонтитул будет вызываться в начале, но он может быть вызван в другое время, и если это возможно, то следует, по возможности, перезаписать исходный заголовок.</span><span class="sxs-lookup"><span data-stu-id="18e5f-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="18e5f-121">Если приложение по какой-либо причине не может сделать это, просто проигнорируйте последующие вызовы **onhead** .</span><span class="sxs-lookup"><span data-stu-id="18e5f-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="18e5f-122">Пользовательский приемник должен передавать свое состояние в приложение для создания, выполнив вызовы метода обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="18e5f-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="18e5f-123">При реализации приемника в качестве COM-объекта может потребоваться предоставить интерфейс [**ивмрегистеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="18e5f-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="18e5f-124">Однако адрес обратного вызова **OnStatus** можно передать в приемник и задать контекст любым способом.</span><span class="sxs-lookup"><span data-stu-id="18e5f-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18e5f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="18e5f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18e5f-126">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="18e5f-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 





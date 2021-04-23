---
title: Использование настраиваемых типов взаимного исключения
description: Использование настраиваемых типов взаимного исключения
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- ивммутуалексклусион
- взаимное исключение, интерфейс Ивммутуалексклусион
- взаимное исключение, пользовательские типы
- профили, пользовательские типы взаимных исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133495"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="6ed40-107">Использование настраиваемых типов взаимного исключения</span><span class="sxs-lookup"><span data-stu-id="6ed40-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="6ed40-108">В профиле можно использовать взаимоисключающие объекты для удовлетворения потребностей пользовательских сценариев.</span><span class="sxs-lookup"><span data-stu-id="6ed40-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="6ed40-109">Передавая значение GUID CLSID \_ вммутекс \_ Unknown в [**Ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), вы сообщаете об объекте взаимного исключения, который используется в пользовательском сценарии.</span><span class="sxs-lookup"><span data-stu-id="6ed40-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="6ed40-110">Необходимо вручную управлять выбором потока при чтении файла с пользовательским взаимоисключающим значением.</span><span class="sxs-lookup"><span data-stu-id="6ed40-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="6ed40-111">Объект модуля чтения будет использовать первый поток, добавляемый в взаимное исключение в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ed40-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="6ed40-112">Чтобы создать настраиваемый объект взаимного исключения и добавить его в профиль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6ed40-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="6ed40-113">Создайте диспетчер профилей, вызвав функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="6ed40-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="6ed40-114">Либо Начните с существующего профиля, либо создайте совершенно новый.</span><span class="sxs-lookup"><span data-stu-id="6ed40-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="6ed40-115">Если вы используете существующий профиль, вызовите один из методов Load интерфейса [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="6ed40-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="6ed40-116">Перейдите к шагу 4.</span><span class="sxs-lookup"><span data-stu-id="6ed40-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="6ed40-117">Если создается совершенно новый профиль, вызовите метод [**ивмпрофилеманажер:: креатимптипрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="6ed40-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="6ed40-118">Добавьте потоки в новый профиль, вызвав [**ивмпрофиле:: креатеневстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span><span class="sxs-lookup"><span data-stu-id="6ed40-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="6ed40-119">При необходимости настройте потоки с помощью методов [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="6ed40-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="6ed40-120">Можно также вызвать **QueryInterface** для доступа к другим интерфейсам в объекте конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="6ed40-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="6ed40-121">**Креатеневстреам** создает только объект конфигурации потока и не влияет на профиль.</span><span class="sxs-lookup"><span data-stu-id="6ed40-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="6ed40-122">После правильной настройки потока необходимо вызвать метод [**ивмпрофиле:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) , чтобы добавить поток в профиль.</span><span class="sxs-lookup"><span data-stu-id="6ed40-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="6ed40-123">Создайте объект взаимного исключения, вызвав [**ивмпрофиле:: креатеневмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="6ed40-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="6ed40-124">Добавьте нужные потоки в объект взаимного исключения, вызвав [**ивмстреамлист:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (доступен непосредственно из [**ивммутуалексклусион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), который наследуется от [**ивмстреамлист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span><span class="sxs-lookup"><span data-stu-id="6ed40-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="6ed40-125">Задайте тип взаимного исключения для настраиваемого объекта, вызвав [**ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="6ed40-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="6ed40-126">Передайте CLSID \_ вммутекс \_ Unknown в качестве типа GUID.</span><span class="sxs-lookup"><span data-stu-id="6ed40-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="6ed40-127">Добавьте настроенный объект взаимного исключения в профиль, вызвав [**ивмпрофиле:: аддмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="6ed40-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ed40-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6ed40-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed40-129">**Интерфейс Ивммутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="6ed40-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="6ed40-130">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="6ed40-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="6ed40-131">**Интерфейс Ивмпрофилеманажер**</span><span class="sxs-lookup"><span data-stu-id="6ed40-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="6ed40-132">**Интерфейс Ивмстреамконфиг**</span><span class="sxs-lookup"><span data-stu-id="6ed40-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="6ed40-133">**Интерфейс Ивмстреамлист**</span><span class="sxs-lookup"><span data-stu-id="6ed40-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="6ed40-134">**Использование взаимного исключения**</span><span class="sxs-lookup"><span data-stu-id="6ed40-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="6ed40-135">**вмкреатепрофилеманажер**</span><span class="sxs-lookup"><span data-stu-id="6ed40-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 





---
title: Использование объекта Active Desktop
description: Эта статья содержит сведения об объекте Активедесктоп, который является частью API оболочки Windows. Этот объект через его интерфейс Иактиведесктоп позволяет добавлять, удалять и изменять элементы на рабочем столе.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Объект Активедесктоп
- Активный рабочий стол
- Перечисление, элементы рабочего стола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487565"
---
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="32553-107">Использование объекта Active Desktop</span><span class="sxs-lookup"><span data-stu-id="32553-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="32553-108">\[Эта функция поддерживается только в Windows XP и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="32553-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="32553-109">\]</span><span class="sxs-lookup"><span data-stu-id="32553-109">\]</span></span>

<span data-ttu-id="32553-110">Эта статья содержит сведения об объекте **активедесктоп** , который является частью API оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="32553-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="32553-111">Этот объект через его интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) позволяет добавлять, удалять и изменять элементы на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="32553-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="32553-112">Общие сведения о интерфейсе Active Desktop</span><span class="sxs-lookup"><span data-stu-id="32553-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="32553-113">Доступ к активному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="32553-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="32553-114">Добавление элемента рабочего стола</span><span class="sxs-lookup"><span data-stu-id="32553-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="32553-115">Перечисление элементов рабочего стола</span><span class="sxs-lookup"><span data-stu-id="32553-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="32553-116">Активный рабочий стол — это функция, появившаяся в Microsoft Internet Explorer 4,0, которая позволяет включать HTML-документы и элементы (например, элементы управления Microsoft ActiveX и Java) непосредственно на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="32553-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="32553-117">Интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , который является частью API оболочки Windows, используется для программного добавления, удаления и изменения элементов на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="32553-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="32553-118">Элементы Active Desktop также можно добавить с помощью файла формата определения канала (CDF).</span><span class="sxs-lookup"><span data-stu-id="32553-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="32553-119">Доступ к активному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="32553-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="32553-120">Чтобы получить доступ к Active Desktop, клиентскому приложению потребуется создать экземпляр объекта Активедесктоп (CLSID \_ активедесктоп) с функцией [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и получить указатель на интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) объекта.</span><span class="sxs-lookup"><span data-stu-id="32553-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="32553-121">В следующем примере показано, как получить указатель на интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="32553-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a><span data-ttu-id="32553-122">Добавление элемента рабочего стола</span><span class="sxs-lookup"><span data-stu-id="32553-122">Adding a Desktop Item</span></span>

<span data-ttu-id="32553-123">Добавить элемент рабочего стола можно с помощью трех методов: [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**Иактиведесктоп:: адддесктопитемвисуи**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)и [**иактиведесктоп:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span><span class="sxs-lookup"><span data-stu-id="32553-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="32553-124">Каждый элемент рабочего стола, добавляемый к активному рабочему столу, должен иметь другой исходный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="32553-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="32553-125">Методы [**иактиведесктоп:: адддесктопитемвисуи**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) и [**Иактиведесктоп:: аддурл**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) предоставляют возможность отображения различных пользовательских интерфейсов, которые можно отобразить перед добавлением элемента рабочего стола на активный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="32553-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="32553-126">Интерфейсы проверяют, хотят ли пользователи добавить элемент рабочего стола в рабочий стол Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="32553-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="32553-127">Кроме того, интерфейсы уведомляют пользователей о любых угрозах безопасности, которые гарантируют параметры зоны безопасности URL-адресов, и запрашивают у пользователей возможность создания подписки для этого элемента рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="32553-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="32553-128">Оба метода также предоставляют способ подавления пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="32553-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="32553-129">Для обновления реестра метод [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) требует вызова [**Иактиведесктоп:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) .</span><span class="sxs-lookup"><span data-stu-id="32553-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="32553-130">Для **иактиведесктоп:: адддесктопитемвисуи** клиентское приложение должно немедленно освободить интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , а затем использовать функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения интерфейса к экземпляру объекта **активедесктоп** , включающего только что добавленный элемент рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="32553-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="32553-131">Метод [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) добавляет указанный элемент рабочего стола в активный рабочий стол без какого-либо пользовательского интерфейса, если это не мешает параметрам зоны безопасности URL.</span><span class="sxs-lookup"><span data-stu-id="32553-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="32553-132">Если параметры зоны безопасности URL-адреса не допускают Добавление элемента рабочего стола без запроса пользователя, то метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="32553-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="32553-133">Для обновления реестра **иактиведесктоп:: адддесктопитем** также требуется вызов [**Иактиведесктоп:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) .</span><span class="sxs-lookup"><span data-stu-id="32553-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="32553-134">В следующем примере показано, как добавить элемент Desktop с помощью метода [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .</span><span class="sxs-lookup"><span data-stu-id="32553-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="32553-135">Перечисление элементов рабочего стола</span><span class="sxs-lookup"><span data-stu-id="32553-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="32553-136">Чтобы перечислить элементы рабочего стола, установленные в настоящий момент на активном рабочем столе, клиентскому приложению необходимо получить общее число элементов рабочего стола, установленных с помощью метода [**иактиведесктоп:: жетдесктопитемкаунт**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) , а затем создать цикл, извлекающий структуру [**компонентов**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) для каждого элемента рабочего стола, вызвав метод [**иактиведесктоп:: жетдесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) , используя индекс элемента рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="32553-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="32553-137">В следующем примере демонстрируется один из способов перечисления элементов рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="32553-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 
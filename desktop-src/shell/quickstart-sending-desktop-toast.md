---
description: В этом кратком руководстве показано, как вызвать всплывающее уведомление из классического приложения.
title: Отправка всплывающего уведомления с рабочего стола
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910767"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="c7798-103">Краткое руководство. отправка всплывающего уведомления с рабочего стола</span><span class="sxs-lookup"><span data-stu-id="c7798-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="c7798-104">В этом кратком руководстве показано, как вызвать всплывающее уведомление из классического приложения.</span><span class="sxs-lookup"><span data-stu-id="c7798-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7798-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="c7798-105">Prerequisites</span></span>

-   <span data-ttu-id="c7798-106">Библиотеки</span><span class="sxs-lookup"><span data-stu-id="c7798-106">Libraries</span></span>
    -   <span data-ttu-id="c7798-107">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="c7798-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="c7798-108">C \# : Windows. winmd</span><span class="sxs-lookup"><span data-stu-id="c7798-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="c7798-109">На начальном экране должен быть установлен ярлык приложения с [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md).</span><span class="sxs-lookup"><span data-stu-id="c7798-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="c7798-110">Однако обратите внимание, что его не нужно закреплять на начальном экране.</span><span class="sxs-lookup"><span data-stu-id="c7798-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="c7798-111">Дополнительные сведения см. [в статье Включение всплывающих уведомлений на рабочем столе с помощью AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span><span class="sxs-lookup"><span data-stu-id="c7798-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="c7798-112">Версия Microsoft Visual Studio, поддерживающая не менее Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7798-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="c7798-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="c7798-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="c7798-114">1. Создание содержимого всплывающего уведомления</span><span class="sxs-lookup"><span data-stu-id="c7798-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="c7798-115">При указании шаблона всплывающего уведомления, включающего изображение, следует учитывать, что классические приложения могут использовать только локальные образы. веб-изображения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c7798-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="c7798-116">Кроме того, путь к локальному файлу изображения должен быть указан как абсолютный (не относительный) путь.</span><span class="sxs-lookup"><span data-stu-id="c7798-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="c7798-117">2. Создание и присоединение обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="c7798-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="c7798-118">Регистрация обработчиков для событий всплывающих уведомлений: активировано, отклонено и сбой.</span><span class="sxs-lookup"><span data-stu-id="c7798-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="c7798-119">Классическое приложение должно иметь по крайней мере подписываться на событие activated, чтобы оно может справиться с ожидаемой активацией приложения из всплывающего уведомления, когда пользователь его выбирает.</span><span class="sxs-lookup"><span data-stu-id="c7798-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="c7798-120">3. отправка всплывающего уведомления</span><span class="sxs-lookup"><span data-stu-id="c7798-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7798-121">Вы должны включить [AppUserModelID](../properties/props-system-appusermodel-id.md) для ярлыка приложения на начальном экране при каждом вызове [**креатетоастнотифиер**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="c7798-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="c7798-122">Если этого не сделать, ваше всплывающее уведомление отображаться не будет.</span><span class="sxs-lookup"><span data-stu-id="c7798-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="c7798-123">4. Обработайте обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="c7798-123">4. Handle the callbacks</span></span>

<span data-ttu-id="c7798-124">Переведите окно приложения на передний план, если оно получает "активированный" обратный вызов из всплывающего уведомления.</span><span class="sxs-lookup"><span data-stu-id="c7798-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="c7798-125">Когда пользователь выбирает всплывающее уведомление, ожидание заключается в том, что приложение будет запускаться в представлении, связанном с содержимым этого всплывающего уведомления.</span><span class="sxs-lookup"><span data-stu-id="c7798-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7798-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c7798-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7798-127">Отправка всплывающих уведомлений из примера классического приложения</span><span class="sxs-lookup"><span data-stu-id="c7798-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="c7798-128">Включение всплывающих уведомлений рабочего стола через AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="c7798-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="c7798-129">XML-схема всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7798-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="c7798-130">[Обзор всплывающих уведомлений](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="c7798-131">[Краткое руководство. отправка всплывающего уведомления](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="c7798-132">[Краткое руководство. отправка всплывающего push-уведомления](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="c7798-133">Рекомендации и контрольный список для всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="c7798-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="c7798-134">[Выбор и использование шаблона всплывающих уведомлений](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="c7798-135">[Как выполнять активацию с помощью всплывающего уведомления](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="c7798-136">[Как принять участие в всплывающих уведомлениях](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="c7798-137">[Выбор шаблона всплывающего уведомления](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="c7798-138">[Параметры звука всплывающего уведомления](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c7798-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 

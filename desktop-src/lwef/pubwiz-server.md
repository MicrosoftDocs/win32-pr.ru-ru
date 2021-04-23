---
title: Разработка Server-Side
description: Функции на стороне сервера взаимодействуют с мастером клиента через объект Windows. external. Сценарий на стороне сервера предоставляет эти функции для реагирования на события мастера и для получения сведений о мастере.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- мастера публикации, проектирование на стороне сервера
- Window. external, мастера публикации
- мастера публикации, Window. external
- мастера публикации, функции сценариев навигации
- сценарии, мастера публикации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987516"
---
# <a name="server-side-design"></a><span data-ttu-id="8c5aa-109">Разработка Server-Side</span><span class="sxs-lookup"><span data-stu-id="8c5aa-109">Server-Side Design</span></span>

<span data-ttu-id="8c5aa-110">Функции на стороне сервера взаимодействуют с мастером клиента через объект **Windows. external** .</span><span class="sxs-lookup"><span data-stu-id="8c5aa-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="8c5aa-111">Сценарий на стороне сервера предоставляет эти функции для реагирования на события мастера и для получения сведений о мастере.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="8c5aa-112">В этом документе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="8c5aa-113">Реализация функций скрипта навигации</span><span class="sxs-lookup"><span data-stu-id="8c5aa-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="8c5aa-114">Onback ()</span><span class="sxs-lookup"><span data-stu-id="8c5aa-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="8c5aa-115">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="8c5aa-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="8c5aa-116">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="8c5aa-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="8c5aa-117">Другие методы и свойства</span><span class="sxs-lookup"><span data-stu-id="8c5aa-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="8c5aa-118">Методы</span><span class="sxs-lookup"><span data-stu-id="8c5aa-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="8c5aa-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c5aa-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="8c5aa-120">См. также</span><span class="sxs-lookup"><span data-stu-id="8c5aa-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="8c5aa-121">Реализация функций скрипта навигации</span><span class="sxs-lookup"><span data-stu-id="8c5aa-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="8c5aa-122">Серверный сценарий на каждой HTML-странице реагирует на кнопки навигации с помощью функций **onback**, **onback** и **onback**.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="8c5aa-123">Эти функции должны быть доступны через **\_ сценарий ихтмлдокумент:: Get** на клиенте и не принимают параметров.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="8c5aa-124">Onback ()</span><span class="sxs-lookup"><span data-stu-id="8c5aa-124">OnBack()</span></span>

-   <span data-ttu-id="8c5aa-125">Реагирует, когда пользователь нажимает кнопку " **назад** " в мастере.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="8c5aa-126">Если текущая страница на стороне сервера является первой страницей на стороне сервера, вызовите метод **Window. external. финалбакк** , чтобы сообщить клиенту о переходе на предыдущую страницу на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="8c5aa-127">Если текущая страница на стороне сервера не является первой страницей на стороне сервера, перейдите на предыдущую страницу на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="8c5aa-128">Эта функция должна быть реализована для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-128">This function must be implemented for each page.</span></span> <span data-ttu-id="8c5aa-129">Любая страница, которая не выполняется, считается недопустимой и отображает страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="8c5aa-130">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="8c5aa-130">OnNext()</span></span>

-   <span data-ttu-id="8c5aa-131">Реагирует, когда пользователь нажимает кнопку " **Далее** " в мастере.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="8c5aa-132">Если текущая страница на стороне сервера является последней страницей на стороне сервера, вызовите метод **Window. external. финалнекст** , чтобы сообщить клиенту о необходимости перехода на следующую страницу на стороне клиента или для завершения работы мастера.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="8c5aa-133">Если текущая страница на стороне сервера не является последней страницей на стороне сервера, перейдите к следующей странице на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="8c5aa-134">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="8c5aa-134">OnCancel()</span></span>

-   <span data-ttu-id="8c5aa-135">Реагирует, когда пользователь нажимает кнопку **"Отмена"** в мастере.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="8c5aa-136">Пользовательский интерфейс должен быть спроектирован таким образом, чтобы пользователь мог отменять его в любое время.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="8c5aa-137">После обработки любой обработки в функции **OnCancel** клиент закрывает мастер.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="8c5aa-138">Другие методы и свойства</span><span class="sxs-lookup"><span data-stu-id="8c5aa-138">Other Methods and Properties</span></span>

<span data-ttu-id="8c5aa-139">Доступ к реализованным клиентом функциям осуществляется через **Windows. external**, как и свойства.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="8c5aa-140">Доступны следующие службы:</span><span class="sxs-lookup"><span data-stu-id="8c5aa-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="8c5aa-141">Методы</span><span class="sxs-lookup"><span data-stu-id="8c5aa-141">Methods</span></span>

-   [<span data-ttu-id="8c5aa-142">**сесеадертекст**</span><span class="sxs-lookup"><span data-stu-id="8c5aa-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="8c5aa-143">**сетвизардбуттонс**</span><span class="sxs-lookup"><span data-stu-id="8c5aa-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="8c5aa-144">**пасспортаусентикате**</span><span class="sxs-lookup"><span data-stu-id="8c5aa-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="8c5aa-145">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c5aa-145">Properties</span></span>

-   <span data-ttu-id="8c5aa-146">[**Заголовок**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c5aa-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="8c5aa-147">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="8c5aa-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="8c5aa-148">В следующем примере кода показан код на стороне сервера для простой страницы мастера, которая реализует страницу ошибки веб-службы.</span><span class="sxs-lookup"><span data-stu-id="8c5aa-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="8c5aa-149">См. также</span><span class="sxs-lookup"><span data-stu-id="8c5aa-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c5aa-150">Проектирование на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="8c5aa-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="8c5aa-151">Регистрация службы</span><span class="sxs-lookup"><span data-stu-id="8c5aa-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 
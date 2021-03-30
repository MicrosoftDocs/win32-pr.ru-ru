---
title: Изменение ресурса диалогового окна Echo
description: Изменение ресурса диалогового окна Echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры страниц свойств Echo
- страницы свойств "подключаемые модули", "Эхо-примеры"
- подключаемые модули обработки цифровых сигналов, примеры страниц свойств
- Подключаемые модули DSP, примеры страниц свойств
- Пример подключаемого модуля "Echo DSP", страницы свойств
- Пример подключаемого модуля "Echo DSP", ресурс диалогового окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331208"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="a4837-109">Изменение ресурса диалогового окна Echo</span><span class="sxs-lookup"><span data-stu-id="a4837-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="a4837-110">Необходимо изменить ресурс диалогового окна, который является пользовательским интерфейсом для объекта страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a4837-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="a4837-111">Вы можете сначала изменить существующее поле и метку поля ввода, чтобы они были полезны для свойства время задержки, а затем добавить второе поле ввода и метку для свойства Mix.</span><span class="sxs-lookup"><span data-stu-id="a4837-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="a4837-112">Чтобы изменить ресурс диалогового окна в Visual C++:</span><span class="sxs-lookup"><span data-stu-id="a4837-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="a4837-113">Перейдите на вкладку **ресаурцевиев** в рабочей области проекта.</span><span class="sxs-lookup"><span data-stu-id="a4837-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="a4837-114">Разверните дерево ресурсов, открыв папку верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="a4837-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="a4837-115">Откройте папку **диалогового окна** .</span><span class="sxs-lookup"><span data-stu-id="a4837-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="a4837-116">Дважды щелкните имя ресурса в диалоговом окне Идд \_ ечопроппаже.</span><span class="sxs-lookup"><span data-stu-id="a4837-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="a4837-117">Редактор ресурсов появится в правой области.</span><span class="sxs-lookup"><span data-stu-id="a4837-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="a4837-118">Изменение существующих ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4837-118">Changing the Existing Resources</span></span>

<span data-ttu-id="a4837-119">Изменение существующих ресурсов страницы свойств для свойства время задержки:</span><span class="sxs-lookup"><span data-stu-id="a4837-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="a4837-120">Сначала измените текст в существующем статическом элементе управления "текст".</span><span class="sxs-lookup"><span data-stu-id="a4837-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="a4837-121">Щелкните правой кнопкой мыши элемент управления и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a4837-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="a4837-122">В поле **Caption (заголовок** ) введите новый заголовок:</span><span class="sxs-lookup"><span data-stu-id="a4837-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="a4837-123">Закройте диалоговое окно Свойства текста.</span><span class="sxs-lookup"><span data-stu-id="a4837-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="a4837-124">Теперь измените имя элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a4837-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="a4837-125">Для этого щелкните элемент управления правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a4837-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="a4837-126">В поле **идентификатор** введите новое имя для элемента управления:</span><span class="sxs-lookup"><span data-stu-id="a4837-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="a4837-127">Закройте диалоговое окно Изменение свойств.</span><span class="sxs-lookup"><span data-stu-id="a4837-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="a4837-128">Сохраните ресурс.</span><span class="sxs-lookup"><span data-stu-id="a4837-128">Save the resource.</span></span>
6.  <span data-ttu-id="a4837-129">Ответьте **Да** , если появится запрос на перезагрузку файла resource. h.</span><span class="sxs-lookup"><span data-stu-id="a4837-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="a4837-130">Перейдите на вкладку **филевиев** в рабочей области проекта.</span><span class="sxs-lookup"><span data-stu-id="a4837-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="a4837-131">Открыть Resource. h</span><span class="sxs-lookup"><span data-stu-id="a4837-131">Open resource.h</span></span>
8.  <span data-ttu-id="a4837-132">Укажите \# ресурс поля для редактирования коэффициента масштабирования (IDC \_ скалефактор) и удалите его.</span><span class="sxs-lookup"><span data-stu-id="a4837-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="a4837-133">Он должен иметь тот же идентификатор, что и IDC \_ DELAYTIME.</span><span class="sxs-lookup"><span data-stu-id="a4837-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="a4837-134">Добавление новых ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4837-134">Adding the New Resources</span></span>

<span data-ttu-id="a4837-135">Чтобы добавить новые ресурсы страницы свойств для свойства "завлажный набор":</span><span class="sxs-lookup"><span data-stu-id="a4837-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="a4837-136">Щелкните вкладку **ресаурцевиев** в рабочей области проекта, чтобы выбрать ее.</span><span class="sxs-lookup"><span data-stu-id="a4837-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="a4837-137">Дважды щелкните имя диалогового окна страницы свойств, Идд \_ ечопроппаже.</span><span class="sxs-lookup"><span data-stu-id="a4837-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="a4837-138">Редактор ресурсов появится в правой области.</span><span class="sxs-lookup"><span data-stu-id="a4837-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="a4837-139">С помощью панели элементов добавьте статический элемент управления текстом и поле ввода на страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="a4837-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="a4837-140">Щелкните правой кнопкой мыши элемент управления "статический текст" и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a4837-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="a4837-141">Введите новое имя для элемента управления "статический текст" в поле " **идентификатор** ":</span><span class="sxs-lookup"><span data-stu-id="a4837-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="a4837-142">Введите заголовок для метки:</span><span class="sxs-lookup"><span data-stu-id="a4837-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="a4837-143">Закройте диалоговое окно Свойства текста.</span><span class="sxs-lookup"><span data-stu-id="a4837-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="a4837-144">Щелкните правой кнопкой мыши поле редактирования и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a4837-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="a4837-145">Введите новое имя для поля ввода в поле **идентификатор** :</span><span class="sxs-lookup"><span data-stu-id="a4837-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="a4837-146">Закройте диалоговое окно Изменение свойств.</span><span class="sxs-lookup"><span data-stu-id="a4837-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="a4837-147">При сохранении проекта может появиться запрос на повторную загрузку Resource. h.</span><span class="sxs-lookup"><span data-stu-id="a4837-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="a4837-148">В этом случае нажмите кнопку **Да** .</span><span class="sxs-lookup"><span data-stu-id="a4837-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="a4837-149">Редактор ресурсов диалогового окна должен добавить имена ресурсов и идентификационные номера в Resource. h для добавленных элементов.</span><span class="sxs-lookup"><span data-stu-id="a4837-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="a4837-150">Если по какой-либо причине это не происходит, необходимо открыть Resource. h и ввести новые записи для элемента управления "метка" и "поле ввода" и назначить каждому уникальному идентификатору.</span><span class="sxs-lookup"><span data-stu-id="a4837-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="a4837-151">Изменение и добавление строковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4837-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="a4837-152">В примере кода мастера подключаемых модулей указывается строковый ресурс с именем ID \_ скалеранжееррор, содержащий сообщение, которое отображается, когда введенные пользователем данные выходят за пределы диапазона.</span><span class="sxs-lookup"><span data-stu-id="a4837-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="a4837-153">Вы можете изменить этот ресурс в соответствии со своими потребностями в качестве значения времени задержки, выполнив следующие действия в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a4837-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="a4837-154">Перейдите на вкладку **ресаурцевиев** .</span><span class="sxs-lookup"><span data-stu-id="a4837-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="a4837-155">Откройте папку **таблицы строк** .</span><span class="sxs-lookup"><span data-stu-id="a4837-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="a4837-156">Дважды щелкните значок **таблицы строк** , чтобы открыть редактор ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4837-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="a4837-157">Дважды щелкните имя ресурса, который необходимо изменить, в данном случае — идентификатор \_ скалеранжееррор.</span><span class="sxs-lookup"><span data-stu-id="a4837-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="a4837-158">Откроется диалоговое окно Свойства строки.</span><span class="sxs-lookup"><span data-stu-id="a4837-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="a4837-159">Измените имя в поле **идентификатор** на идентификатор \_ делайранжееррор.</span><span class="sxs-lookup"><span data-stu-id="a4837-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="a4837-160">Измените текст в поле **Caption (заголовок** ):</span><span class="sxs-lookup"><span data-stu-id="a4837-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="a4837-161">Закройте диалоговое окно Свойства строки.</span><span class="sxs-lookup"><span data-stu-id="a4837-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="a4837-162">Затем добавьте новый строковый ресурс для сообщения об ошибке свойства Mix.</span><span class="sxs-lookup"><span data-stu-id="a4837-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="a4837-163">Дважды щелкните пустую строку в нижней части редактора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4837-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="a4837-164">Измените имя в поле **идентификатор** на идентификатор \_ миксранжееррор.</span><span class="sxs-lookup"><span data-stu-id="a4837-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="a4837-165">Добавьте следующий текст в поле **Caption (заголовок** ):</span><span class="sxs-lookup"><span data-stu-id="a4837-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="a4837-166">Закройте диалоговое окно Свойства строки.</span><span class="sxs-lookup"><span data-stu-id="a4837-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="a4837-167">В таблице строк необходимо изменить еще два значения.</span><span class="sxs-lookup"><span data-stu-id="a4837-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="a4837-168">ИДЕНТИФИКАТОРы \_ FRIENDLYNAME — это имя, которое отображается в пользовательском интерфейсе проигрывателя Windows Media для идентификации подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a4837-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="a4837-169">Описание ИДЕНТИФИКАТОРов \_ позволяет сообщить пользователю о подключаемом модуле.</span><span class="sxs-lookup"><span data-stu-id="a4837-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="a4837-170">Обе эти строки передаются в качестве параметров в функцию **ивмпмедиаплугинрегистрар:: вмпрегистерплайерплугин** , которая вызывается в методе DllRegisterServer в ечодлл. cpp.</span><span class="sxs-lookup"><span data-stu-id="a4837-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4837-171">См. также</span><span class="sxs-lookup"><span data-stu-id="a4837-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4837-172">**Изменение страницы свойств «пример эха»**</span><span class="sxs-lookup"><span data-stu-id="a4837-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





---
title: Обслуживание сведений о сеансе
description: Обслуживание сведений о сеансе
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Интернет-магазины проигрывателя Windows Media, сохранение сведений о сеансе
- Интернет-магазины, обслуживание сведений о сеансах
- Тип 2 Интернет-магазинов, обслуживание сведений о сеансе
- Интернет-магазины проигрывателя Windows Media, сведения о сеансе
- Интернет-магазины, сведения о сеансе
- Тип 2 Интернет-магазинов, сведения о сеансе
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- Обслуживание сведений о сеансе
- сведения о сеансе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332680"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="3fcdf-117">Обслуживание сведений о сеансе</span><span class="sxs-lookup"><span data-stu-id="3fcdf-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="3fcdf-118">Как в примере сохраняются сведения</span><span class="sxs-lookup"><span data-stu-id="3fcdf-118">How the Sample Stores Information</span></span>

<span data-ttu-id="3fcdf-119">Пример веб-страницы сохраняет данные с помощью файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="3fcdf-120">Файлы cookie — это просто постоянные пары "имя-значение", которые могут храниться в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="3fcdf-121">При закрытии веб-страницы запускается функция **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="3fcdf-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="3fcdf-122">**Shutdown** вызывает функцию **сетпендингкукиес**.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="3fcdf-123">Эта функция выполняет перебор списка загрузки коллекции, хранящегося в раскрывающемся списке с именем Селдлк.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="3fcdf-124">Если коллекция загрузки содержит неполные элементы, функция вызывает метод **SetCookie**, передавая имя и значение.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="3fcdf-125">Строка имени определяется путем добавления целочисленного значения к значению константы **вмпдлк**, которое хранится в переменной с именем g \_ спрекукие.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="3fcdf-126">Например, для третьей ожидающей коллекции загрузки имя файла cookie будет «WMPDLC2», так как механизм подсчета отсчитывается от нуля.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="3fcdf-127">При создании каждого файла cookie функция увеличивает глобальную переменную g в \_ ожидании для сохранения числа незавершенных Скачиваний.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="3fcdf-128">Ниже приведен код, который можно воспроизвести для вашего удобства:</span><span class="sxs-lookup"><span data-stu-id="3fcdf-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="3fcdf-129">**Исдлккомплете** — это вспомогательная функция, которая просто просматривает каждый элемент загрузки в коллекции загрузки, чтобы определить, ожидает ли какой-либо элемент.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="3fcdf-130">Если имеется ожидающий элемент, функция возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="3fcdf-131">**SetCookie** — это функция, которая создает файл cookie.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="3fcdf-132">Когда **сетпендингкукиес** возвращает, **Завершение работы** создает файл cookie Count, который сохраняет значение из переменной g \_ в ожидании.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="3fcdf-133">Это значение важно, так как веб-странице требуется способ определить количество файлов cookie для извлечения при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="3fcdf-134">Имя файла cookie счетчика хранится в переменной с именем g \_ скаунткукие.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="3fcdf-135">Получение сведений в примере</span><span class="sxs-lookup"><span data-stu-id="3fcdf-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="3fcdf-136">При загрузке веб-страницы выполняется функция **init** .</span><span class="sxs-lookup"><span data-stu-id="3fcdf-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="3fcdf-137">Во-первых, функция вызывает **жетпендингдлкаунт** для получения файла cookie счетчика.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="3fcdf-138">Затем оно сохраняет это значение в переменной с именем g \_ Pending.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="3fcdf-139">Затем вызывается функция **популатедллист** для получения каждого файла cookie сеанса загрузки и добавления его идентификатора в раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="3fcdf-140">Ниже приведен код для этой функции:</span><span class="sxs-lookup"><span data-stu-id="3fcdf-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="3fcdf-141">Функция **клеарлист** удаляет все элементы из списка.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="3fcdf-142">Затем функция входит в цикл.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-142">The function then enters a loop.</span></span> <span data-ttu-id="3fcdf-143">Каждое имя файла cookie создается как строка, а затем файл cookie извлекается путем вызова вспомогательной **функции.**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="3fcdf-144">После извлечения файл cookie удаляется путем вызова **делкукие**.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="3fcdf-145">Если файл cookie имеет значение, значение добавляется в список.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="3fcdf-146">Это действие инициирует событие **onChange** для списка селдлк, который, в свою очередь, вызывает функцию обработчика с именем **онселектдлк**.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="3fcdf-147">Это та же функция, которая выполняется, когда пользователь выбирает коллекцию загрузки. Это код, который заполняет окно списка элементов загрузки.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fcdf-148">См. также</span><span class="sxs-lookup"><span data-stu-id="3fcdf-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fcdf-149">**Использование диспетчера загрузки**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 





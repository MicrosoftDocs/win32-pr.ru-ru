---
title: Получение сведений о состоянии
description: Получение сведений о состоянии
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Интернет-магазины проигрывателя Windows Media, получение состояния
- Интернет-магазины, получение состояния
- Тип 2 Интернет-магазинов, получение состояния
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- получение состояния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778257"
---
# <a name="retrieving-status-information"></a><span data-ttu-id="a6d08-113">Получение сведений о состоянии</span><span class="sxs-lookup"><span data-stu-id="a6d08-113">Retrieving Status Information</span></span>

<span data-ttu-id="a6d08-114">Сведения о состоянии обновляются с помощью таймера, созданного в функции **init** .</span><span class="sxs-lookup"><span data-stu-id="a6d08-114">Status information is updated using the timer created in the **Init** function.</span></span> <span data-ttu-id="a6d08-115">Все состояния обновляются с помощью одного и того же таймера.</span><span class="sxs-lookup"><span data-stu-id="a6d08-115">All status is updated using the same timer.</span></span> <span data-ttu-id="a6d08-116">Имя функции для события таймера — **OnTime**.</span><span class="sxs-lookup"><span data-stu-id="a6d08-116">The name of the function for the timer event is **OnTimer**.</span></span>

<span data-ttu-id="a6d08-117">**OnTime** определяет отображаемые сведения на основе выбора пользователя, который хранится в глобальной переменной с именем g \_ окуррентдлитем.</span><span class="sxs-lookup"><span data-stu-id="a6d08-117">**OnTimer** determines the information to display based upon the user selection, which is stored in the global variable named g\_oCurrentDLItem.</span></span> <span data-ttu-id="a6d08-118">Сначала функция проверяет допустимость значений размера или хода выполнения и создает строку для каждого варианта.</span><span class="sxs-lookup"><span data-stu-id="a6d08-118">The function first tests whether the size or progress values are valid and creates a string for each case.</span></span>


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



<span data-ttu-id="a6d08-119">Если значение допустимо, строка представляет число байтов.</span><span class="sxs-lookup"><span data-stu-id="a6d08-119">If a value is valid, the string represents the byte count.</span></span> <span data-ttu-id="a6d08-120">Если значение недопустимо, например-1, строка предоставляет сообщение, сообщающее пользователю о том, что информация еще недоступна.</span><span class="sxs-lookup"><span data-stu-id="a6d08-120">If the value is not valid, such as -1, the string provides a message to inform the user that the information is not yet available.</span></span>

<span data-ttu-id="a6d08-121">Затем блок **переключателя** определяет, завершено ли скачивание для выбранного элемента или отменено.</span><span class="sxs-lookup"><span data-stu-id="a6d08-121">Next, a **switch** block determines whether the download for the selected item is completed or canceled.</span></span> <span data-ttu-id="a6d08-122">Если оба варианта имеют значение true, значения переменных размера или хода выполнения обновляются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="a6d08-122">If either case is true, the value of the variables Size or Progress is updated accordingly.</span></span>


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



<span data-ttu-id="a6d08-123">Наконец, сведения о состоянии отображаются в элементе DIV с именем длстате.</span><span class="sxs-lookup"><span data-stu-id="a6d08-123">Finally, the status information is displayed in the DIV element named dlstate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6d08-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a6d08-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d08-125">**Использование диспетчера загрузки**</span><span class="sxs-lookup"><span data-stu-id="a6d08-125">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 





---
title: Начало загрузки
description: Начало загрузки
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Интернет-магазины проигрывателя Windows Media, запуск загрузки
- Интернет-магазины, запуск загрузки
- Тип 2 Интернет-магазинов, запуск загрузок
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- Запуск загрузок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411333"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="25801-113">Начало загрузки</span><span class="sxs-lookup"><span data-stu-id="25801-113">Starting the Downloads</span></span>

<span data-ttu-id="25801-114">Загрузка начинается при нажатии пользователем кнопки **загрузить**.</span><span class="sxs-lookup"><span data-stu-id="25801-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="25801-115">Эта кнопка называется Бтндовнлоад в коде, а функция обработчика событий для события **OnClick** называется "OnClick".</span><span class="sxs-lookup"><span data-stu-id="25801-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="25801-116">При первом скачивании сначала создается пустой объект **довнлоадколлектион** , который назначается локальной переменной.</span><span class="sxs-lookup"><span data-stu-id="25801-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="25801-117">Затем функция запускает каждый из пяти элементов, загружая и сохраняющая возвращенный объект **довнлоадитем** в массиве.</span><span class="sxs-lookup"><span data-stu-id="25801-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="25801-118">Затем код обновляет элементы пользовательского интерфейса со сведениями о загружаемой коллекции и ее элементах загрузки.</span><span class="sxs-lookup"><span data-stu-id="25801-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25801-119">См. также</span><span class="sxs-lookup"><span data-stu-id="25801-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25801-120">**Использование диспетчера загрузки**</span><span class="sxs-lookup"><span data-stu-id="25801-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 





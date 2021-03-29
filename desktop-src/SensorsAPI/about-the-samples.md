---
description: В Windows SDK содержатся полезные примеры кода и средства, помогающие понять и использовать платформу датчиков и расположения Windows, а также связанные интерфейсы API.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: О примерах и средствах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912236"
---
# <a name="about-the-samples-and-tools"></a><span data-ttu-id="21094-103">О примерах и средствах</span><span class="sxs-lookup"><span data-stu-id="21094-103">About the Samples and Tools</span></span>

<span data-ttu-id="21094-104">В Windows SDK содержатся полезные примеры кода и средства, помогающие понять и использовать платформу датчиков и расположения Windows, а также связанные интерфейсы API.</span><span class="sxs-lookup"><span data-stu-id="21094-104">The Windows SDK includes useful code samples and tools to help you understand and use the Windows Sensor and Location platform and related APIs.</span></span>

## <a name="samples"></a><span data-ttu-id="21094-105">Примеры</span><span class="sxs-lookup"><span data-stu-id="21094-105">Samples</span></span>

<span data-ttu-id="21094-106">Windows SDK включает следующие примеры API датчика.</span><span class="sxs-lookup"><span data-stu-id="21094-106">The Windows SDK includes the following Sensor API samples.</span></span> <span data-ttu-id="21094-107">Примеры API датчика можно найти в папке \\ Samples \\ винуи \\ Sensors, где вы установили Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="21094-107">You can find the Sensor API samples in the folder named \\Samples\\winui\\Sensors, where you installed the Windows SDK.</span></span> <span data-ttu-id="21094-108">Например, если вы установили Windows SDK на диске C, вы найдете примеры в следующей папке: C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ винуи \\ sensors.</span><span class="sxs-lookup"><span data-stu-id="21094-108">For example, if you installed the Windows SDK on drive C, you would find the samples in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\winui\\Sensors.</span></span>



| <span data-ttu-id="21094-109">Имя примера</span><span class="sxs-lookup"><span data-stu-id="21094-109">Sample name</span></span>       | <span data-ttu-id="21094-110">Описание</span><span class="sxs-lookup"><span data-stu-id="21094-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21094-111">амбиентлигхтаваре</span><span class="sxs-lookup"><span data-stu-id="21094-111">AmbientLightAware</span></span> | <span data-ttu-id="21094-112">В этом примере MFC показано, как использовать API датчика путем считывания данных из датчиков внешнего освещения на компьютере и изменения размера текста в соответствии с условиями освещения.</span><span class="sxs-lookup"><span data-stu-id="21094-112">This MFC sample shows how to use the Sensor API by reading data from ambient light sensors on the computer and changing text size according to the lighting conditions.</span></span> <span data-ttu-id="21094-113">Можно увидеть код, демонстрирующий управление событиями и запрос разрешений пользователя.</span><span class="sxs-lookup"><span data-stu-id="21094-113">You can see code that shows how to manage events and how to request user permissions.</span></span> <span data-ttu-id="21094-114">Вы также можете увидеть пример управления пользовательским интерфейсом на основе различных условий освещения.</span><span class="sxs-lookup"><span data-stu-id="21094-114">You can also see an example of how to manage the user interface based on varying lighting conditions.</span></span> <span data-ttu-id="21094-115">Дополнительные сведения см. в разделе [создание Light-Aware пользовательских интерфейсов](creating-light-aware-user-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="21094-115">For more information, see [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).</span></span><br/> <span data-ttu-id="21094-116">Для сборки этого образца необходимо установить Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="21094-116">You must have Visual Studio 2008 installed to build this sample.</span></span><br/> |



 

<span data-ttu-id="21094-117">Дополнительные сведения см. в файле с именем ReadMe.txt, который входит в состав примера.</span><span class="sxs-lookup"><span data-stu-id="21094-117">For more information, see the file named ReadMe.txt that is included with the sample.</span></span>

<span data-ttu-id="21094-118">Вы также можете скачать пример Амбиентлигхтаваре из коллекции кода.</span><span class="sxs-lookup"><span data-stu-id="21094-118">You can also download the AmbientLightAware sample from Code Gallery.</span></span> <span data-ttu-id="21094-119">Дополнительные сведения см. на странице загрузки с [поддержкой внешнего источника](/samples/browse/?redirectedfrom=MSDN-samples) .</span><span class="sxs-lookup"><span data-stu-id="21094-119">For more information, see the [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) download page.</span></span>

## <a name="tools"></a><span data-ttu-id="21094-120">Инструменты</span><span class="sxs-lookup"><span data-stu-id="21094-120">Tools</span></span>

<span data-ttu-id="21094-121">В Windows SDK содержится виртуальный датчик освещения, который можно использовать для имитации устройства аппаратного датчика.</span><span class="sxs-lookup"><span data-stu-id="21094-121">The Windows SDK includes a virtual light sensor that you can use to simulate a hardware-based light sensor device.</span></span> <span data-ttu-id="21094-122">Это средство можно использовать для передачи данных в образец Амбиентлигхтаваре, чтобы увидеть, как работает код в образце.</span><span class="sxs-lookup"><span data-stu-id="21094-122">You can use this tool to provide data to the AmbientLightAware sample to see how the code in the sample works.</span></span>

<span data-ttu-id="21094-123">В следующей таблице описаны файлы, которые необходимо использовать для запуска датчика виртуальной лампочки.</span><span class="sxs-lookup"><span data-stu-id="21094-123">The following table describes the files you must use to run the virtual light sensor.</span></span> <span data-ttu-id="21094-124">Эти файлы можно найти в папке bin, где вы установили Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="21094-124">You can find these files in the folder named Bin, where you installed the Windows SDK.</span></span> <span data-ttu-id="21094-125">Например, если вы установили Windows SDK на диске C на 32-разрядном компьютере, можно найти файлы виртуального датчика в следующей папке: C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="21094-125">For example, if you installed the Windows SDK on drive C on a 32-bit computer, you would find the virtual light sensor files in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Bin.</span></span> <span data-ttu-id="21094-126">На 64-разрядных компьютерах необходимо использовать 64-разрядную версию средства.</span><span class="sxs-lookup"><span data-stu-id="21094-126">On 64-bit computers, you must use the 64-bit version of the tool.</span></span> <span data-ttu-id="21094-127">В Windows SDK 64-разрядные средства находятся во вложенной папке с именем x64.</span><span class="sxs-lookup"><span data-stu-id="21094-127">In the Windows SDK, 64-bit tools are located in the subfolder named x64.</span></span>



| <span data-ttu-id="21094-128">Имя файла</span><span class="sxs-lookup"><span data-stu-id="21094-128">File name</span></span>                    | <span data-ttu-id="21094-129">Описание</span><span class="sxs-lookup"><span data-stu-id="21094-129">Description</span></span>                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21094-130">VirtualLightSensor.exe</span><span class="sxs-lookup"><span data-stu-id="21094-130">VirtualLightSensor.exe</span></span>       | <span data-ttu-id="21094-131">Эта программа предоставляет элемент управления "ползунок", позволяющий изменять уровень данных освещения, которые включаются в отчеты виртуального датчика.</span><span class="sxs-lookup"><span data-stu-id="21094-131">This program provides a slider control that enables you to change the level of the light data that the virtual sensor reports.</span></span> |
| <span data-ttu-id="21094-132">VirtualLightSensorDriver.dll</span><span class="sxs-lookup"><span data-stu-id="21094-132">VirtualLightSensorDriver.dll</span></span> | <span data-ttu-id="21094-133">Логический драйвер датчика, имитирующий датчик освещения.</span><span class="sxs-lookup"><span data-stu-id="21094-133">The logical sensor driver that simulates a light sensor.</span></span>                                                                       |
| <span data-ttu-id="21094-134">Виртуаллигхтсенсордривер. INF</span><span class="sxs-lookup"><span data-stu-id="21094-134">VirtualLightSensorDriver.inf</span></span> | <span data-ttu-id="21094-135">INF-файл для драйвера виртуального источника освещения.</span><span class="sxs-lookup"><span data-stu-id="21094-135">The INF file for the virtual light sensor driver.</span></span>                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a><span data-ttu-id="21094-136">Установка виртуального источника освещения</span><span class="sxs-lookup"><span data-stu-id="21094-136">Installing the Virtual Light Sensor</span></span>

<span data-ttu-id="21094-137">Прежде чем использовать приложение виртуального источника освещения, необходимо установить драйвер логического датчика.</span><span class="sxs-lookup"><span data-stu-id="21094-137">Before you use the virtual light sensor application, you must install the logical sensor driver.</span></span> <span data-ttu-id="21094-138">Выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="21094-138">Follow these steps:</span></span>

1.  <span data-ttu-id="21094-139">Откройте командное окно от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="21094-139">Open a command window as an administrator.</span></span>
2.  <span data-ttu-id="21094-140">Перейдите в папку Windows SDK bin.</span><span class="sxs-lookup"><span data-stu-id="21094-140">Change to the Windows SDK Bin folder.</span></span>
3.  <span data-ttu-id="21094-141">Введите **PnPUtil-a виртуаллигхтсенсордривер. INF**.</span><span class="sxs-lookup"><span data-stu-id="21094-141">Type **pnputil -a VirtualLightSensorDriver.inf**.</span></span>
4.  <span data-ttu-id="21094-142">При появлении запроса щелкните **установить это программное обеспечение с драйвером**.</span><span class="sxs-lookup"><span data-stu-id="21094-142">When prompted, click **Install this driver software anyway**.</span></span>
5.  <span data-ttu-id="21094-143">Дождитесь, пока командное окно сообщит о том, что драйвер успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="21094-143">Wait for the command window to report that the driver was successfully installed.</span></span>

### <a name="running-the-virtual-light-sensor"></a><span data-ttu-id="21094-144">Запуск виртуального датчика освещения</span><span class="sxs-lookup"><span data-stu-id="21094-144">Running the Virtual Light Sensor</span></span>

<span data-ttu-id="21094-145">Чтобы запустить датчик виртуального источника, просто дважды щелкните EXE-файл.</span><span class="sxs-lookup"><span data-stu-id="21094-145">To run the virtual light sensor, simply double-click the .exe file.</span></span> <span data-ttu-id="21094-146">При появлении запроса обязательно включите датчик.</span><span class="sxs-lookup"><span data-stu-id="21094-146">Be sure to enable the sensor, when prompted.</span></span>

<span data-ttu-id="21094-147">При запуске программы можно заметить задержку до того, как датчик станет доступным.</span><span class="sxs-lookup"><span data-stu-id="21094-147">When you run the program, you may notice that there is a delay before the sensor becomes available.</span></span> <span data-ttu-id="21094-148">В пользовательском интерфейсе датчика виртуального источника отображается сообщение "ожидание" в заголовке окна, а логический диспетчер датчиков создает узел устройства для логического датчика.</span><span class="sxs-lookup"><span data-stu-id="21094-148">The virtual light sensor user interface will display the message "Waiting" in the title bar while the logical sensor manager creates a device node for the logical sensor.</span></span> <span data-ttu-id="21094-149">После выхода из ожидающего сообщения можно использовать ползунок, чтобы задать уровень вывода Lux для виртуального датчика освещения.</span><span class="sxs-lookup"><span data-stu-id="21094-149">After the waiting message goes away, you can use the slider to set the lux output level for the virtual light sensor.</span></span>

<span data-ttu-id="21094-150">На следующем рисунке показан пользовательский интерфейс датчика виртуального источника в состоянии готовности.</span><span class="sxs-lookup"><span data-stu-id="21094-150">The following image shows the virtual light sensor user interface in its ready state.</span></span>

![Пользовательский интерфейс виртуального источника датчика](images/virtuallightsensor.png)

## <a name="related-topics"></a><span data-ttu-id="21094-152">См. также</span><span class="sxs-lookup"><span data-stu-id="21094-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21094-153">О логических датчиках</span><span class="sxs-lookup"><span data-stu-id="21094-153">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> <dt>

[<span data-ttu-id="21094-154">**\_Категория датчика \_ : светло**</span><span class="sxs-lookup"><span data-stu-id="21094-154">**SENSOR\_CATEGORY\_LIGHT**</span></span>](sensor-category-light.md)
</dt> </dl>

 


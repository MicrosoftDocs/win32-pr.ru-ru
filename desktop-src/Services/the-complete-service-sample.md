---
description: 'Дополнительные сведения: полный пример службы'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Полный пример службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664089"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="97e7e-103">Полный пример службы</span><span class="sxs-lookup"><span data-stu-id="97e7e-103">The Complete Service Sample</span></span>

<span data-ttu-id="97e7e-104">Темы в этом разделе образуют полный пример службы:</span><span class="sxs-lookup"><span data-stu-id="97e7e-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="97e7e-105">[Sample.MC](sample-mc.md) (содержит сообщения об ошибках)</span><span class="sxs-lookup"><span data-stu-id="97e7e-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="97e7e-106">[SVC. cpp](svc-cpp.md) (содержит код службы)</span><span class="sxs-lookup"><span data-stu-id="97e7e-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="97e7e-107">[Свкконфиг. cpp](svcconfig-cpp.md) (содержит код конфигурации службы)</span><span class="sxs-lookup"><span data-stu-id="97e7e-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="97e7e-108">[Свкконтрол. cpp](svccontrol-cpp.md) (содержит код управления службами)</span><span class="sxs-lookup"><span data-stu-id="97e7e-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="97e7e-109">Создание службы</span><span class="sxs-lookup"><span data-stu-id="97e7e-109">Building the Service</span></span>

<span data-ttu-id="97e7e-110">Следующая процедура описывает, как создать службу и зарегистрировать БИБЛИОТЕКУ сообщений о событиях.</span><span class="sxs-lookup"><span data-stu-id="97e7e-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="97e7e-111">**Создание службы и регистрация библиотеки DLL сообщений о событиях**</span><span class="sxs-lookup"><span data-stu-id="97e7e-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="97e7e-112">Создайте библиотеку DLL сообщений из Sample.mc, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="97e7e-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="97e7e-113">**MC-U sample.mc**</span><span class="sxs-lookup"><span data-stu-id="97e7e-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="97e7e-114">**RC-r Sample. RC**</span><span class="sxs-lookup"><span data-stu-id="97e7e-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="97e7e-115">**Link-DLL--out:sample.dll Sample. Res**</span><span class="sxs-lookup"><span data-stu-id="97e7e-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="97e7e-116">Создавайте Svc.exe, SvcConfig.exe и SvcControl.exe из SVC. cpp, Свкконфиг. cpp и Свкконтрол. cpp соответственно.</span><span class="sxs-lookup"><span data-stu-id="97e7e-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="97e7e-117">Создайте раздел реестра **hKey \_ локальный \_ компьютер \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ \\ SvcName** и добавьте в этот раздел следующие значения реестра.</span><span class="sxs-lookup"><span data-stu-id="97e7e-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="97e7e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="97e7e-118">Value</span></span>                              | <span data-ttu-id="97e7e-119">Тип</span><span class="sxs-lookup"><span data-stu-id="97e7e-119">Type</span></span>       | <span data-ttu-id="97e7e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="97e7e-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="97e7e-121">**Евентмессажефиле**  =  *\_ путь к библиотеке DLL*</span><span class="sxs-lookup"><span data-stu-id="97e7e-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="97e7e-122">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="97e7e-122">REG\_SZ</span></span>    | <span data-ttu-id="97e7e-123">Путь к библиотеке DLL, содержащей только ресурсы, которые содержат строки, которые служба может записать в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="97e7e-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="97e7e-124">**Типессуппортед** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="97e7e-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="97e7e-125">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="97e7e-125">REG\_DWORD</span></span> | <span data-ttu-id="97e7e-126">Битовая маска, указывающая Поддерживаемые типы событий.</span><span class="sxs-lookup"><span data-stu-id="97e7e-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="97e7e-127">Значение 0x000000007 указывает, что поддерживаются все типы.</span><span class="sxs-lookup"><span data-stu-id="97e7e-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="97e7e-128">Тестирование службы</span><span class="sxs-lookup"><span data-stu-id="97e7e-128">Testing the Service</span></span>

<span data-ttu-id="97e7e-129">В следующей процедуре описывается тестирование службы.</span><span class="sxs-lookup"><span data-stu-id="97e7e-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="97e7e-130">**Проверка службы**</span><span class="sxs-lookup"><span data-stu-id="97e7e-130">**To test the service**</span></span>

1.  <span data-ttu-id="97e7e-131">В панели управления запустите приложение **службы** .</span><span class="sxs-lookup"><span data-stu-id="97e7e-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="97e7e-132">(В следующих шагах используйте клавишу F5, чтобы обновить отображение после выполнения команды, которая изменяет сведения в приложении **служб** .)</span><span class="sxs-lookup"><span data-stu-id="97e7e-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="97e7e-133">Выполните следующую команду, чтобы установить службу:</span><span class="sxs-lookup"><span data-stu-id="97e7e-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="97e7e-134">**Установка SVC**</span><span class="sxs-lookup"><span data-stu-id="97e7e-134">**svc install**</span></span>

    <span data-ttu-id="97e7e-135">Служба в консоли производит запись "служба успешно установлена", если операция выполняется успешно, или в противном случае — сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="97e7e-136">Если установка службы будет выполнена, служба отобразится в приложении **службы** .</span><span class="sxs-lookup"><span data-stu-id="97e7e-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="97e7e-137">Обратите внимание, что для **Name** задано значение "SvcName", **Описание** и **состояние** пусты, а для **типа запуска** задано значение "вручную".</span><span class="sxs-lookup"><span data-stu-id="97e7e-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="97e7e-138">Выполните следующую команду, чтобы запустить службу:</span><span class="sxs-lookup"><span data-stu-id="97e7e-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="97e7e-139">**свкконтрол запустить SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="97e7e-140">Если операция выполнена, программа управления службой запишет "Ожидание запуска службы..." а затем "служба успешно запущена" на консоли.</span><span class="sxs-lookup"><span data-stu-id="97e7e-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="97e7e-141">В противном случае программа записывает сообщение об ошибке в консоль.</span><span class="sxs-lookup"><span data-stu-id="97e7e-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="97e7e-142">Если служба успешно запускается, для параметра **Status** задается значение "запущено".</span><span class="sxs-lookup"><span data-stu-id="97e7e-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="97e7e-143">Код функции [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) выполняется SCM.</span><span class="sxs-lookup"><span data-stu-id="97e7e-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="97e7e-144">При возникновении ошибки служба будет записывать сообщение об ошибке в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="97e7e-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="97e7e-145">Это сообщение содержит имя функции, которая завершилась ошибкой, и код ошибки, возвращенный в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="97e7e-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="97e7e-146">Выполните следующую команду, чтобы обновить описание службы:</span><span class="sxs-lookup"><span data-stu-id="97e7e-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="97e7e-147">**свкконфиг описание SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="97e7e-148">Программа настройки службы записывает сообщение "описание службы успешно обновлено" на консоль, если операция выполнена успешно, или в противном случае — сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="97e7e-149">Если обновление завершилось с ошибкой, в поле **Описание** задается значение "это описание теста".</span><span class="sxs-lookup"><span data-stu-id="97e7e-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="97e7e-150">Выполните следующую команду, чтобы запросить конфигурацию службы:</span><span class="sxs-lookup"><span data-stu-id="97e7e-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="97e7e-151">**свкконфиг запрос SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="97e7e-152">Программа настройки службы записывает сведения о конфигурации службы в консоль при условии, что операция завершилась с ошибкой, или в противном случае — сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="97e7e-153">Чтобы изменить список DACL службы, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="97e7e-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="97e7e-154">**свкконтрол DACL SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="97e7e-155">Программа настройки службы выполняет запись "DACL службы успешно обновлена" на консоль, если операция выполнена успешно, или в противном случае — сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="97e7e-156">Чтобы отключить службу, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="97e7e-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="97e7e-157">**свкконфиг отключить SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="97e7e-158">Программа настройки службы в консоли выполняет запись "служба отключена успешно", если операция выполняется успешно, или в противном случае — сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="97e7e-159">Если служба успешно отключена, для параметра **Тип запуска** задается значение Disabled (отключено).</span><span class="sxs-lookup"><span data-stu-id="97e7e-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="97e7e-160">Чтобы включить службу, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="97e7e-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="97e7e-161">**свкконфиг включить SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="97e7e-162">Программа настройки службы в консоли записывает "служба успешно включена", если операция выполняется успешно, или в противном случае — сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="97e7e-163">Если служба успешно включена, для параметра **Тип запуска** устанавливается значение вручную.</span><span class="sxs-lookup"><span data-stu-id="97e7e-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="97e7e-164">Чтобы отключить службу, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="97e7e-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="97e7e-165">**свкконтрол останавливает SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="97e7e-166">Если операция завершится с ошибкой, программа управления службой запишет "ожидание службы ожидается..." а затем "служба успешно остановлена" на консоли.</span><span class="sxs-lookup"><span data-stu-id="97e7e-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="97e7e-167">В противном случае программа записывает сообщение об ошибке в консоль.</span><span class="sxs-lookup"><span data-stu-id="97e7e-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="97e7e-168">Если служба завершается успешно, **состояние** остается пустым.</span><span class="sxs-lookup"><span data-stu-id="97e7e-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="97e7e-169">Если не удается завершить работу службы, программа управления службой записывает в журнал событий сообщение об ошибке, содержащее имя функции, которая завершилась ошибкой, и код ошибки, возвращенный в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="97e7e-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="97e7e-170">Выполните следующую команду, чтобы удалить службу:</span><span class="sxs-lookup"><span data-stu-id="97e7e-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="97e7e-171">**свкконфиг удалить SvcName**</span><span class="sxs-lookup"><span data-stu-id="97e7e-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="97e7e-172">Программа настройки службы записывает "служба успешно удалена" на консоль, если операция выполняется успешно, или в противном случае — сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="97e7e-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="97e7e-173">Если служба успешно удалена, она больше не отображается в приложении **службы** .</span><span class="sxs-lookup"><span data-stu-id="97e7e-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="97e7e-174">(Обратите внимание, что при попытке удалить службу, которая не остановлена, операция завершается с ошибкой, но для параметра **Тип запуска** устанавливается значение "отключено", а запись службы будет удалена при перезапуске системы или при завершении работы службы с помощью диспетчера задач.)</span><span class="sxs-lookup"><span data-stu-id="97e7e-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="97e7e-175">См. также</span><span class="sxs-lookup"><span data-stu-id="97e7e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97e7e-176">Использование служб</span><span class="sxs-lookup"><span data-stu-id="97e7e-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 

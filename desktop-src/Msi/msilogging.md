---
description: Свойство Мсилоггинг задает режим ведения журнала по умолчанию для пакета установщик Windows.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Мсилоггинг, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679860"
---
# <a name="msilogging-property"></a><span data-ttu-id="5aa63-103">Мсилоггинг, свойство</span><span class="sxs-lookup"><span data-stu-id="5aa63-103">MsiLogging property</span></span>

<span data-ttu-id="5aa63-104">Свойство **мсилоггинг** задает режим ведения журнала по умолчанию для пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="5aa63-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="5aa63-105">Если это необязательное свойство имеется в [таблице свойств](property-table.md), установщик создает файл журнала с именем MSI \* . Журналь.</span><span class="sxs-lookup"><span data-stu-id="5aa63-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="5aa63-106">Полный путь к файлу журнала предоставляется значением свойства [**мсилогфилелокатион**](msilogfilelocation.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa63-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="5aa63-107">Значение</span><span class="sxs-lookup"><span data-stu-id="5aa63-107">Value</span></span>

<span data-ttu-id="5aa63-108">Значение этого свойства должно быть строкой следующих символов, определяющих режим ведения журнала по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5aa63-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="5aa63-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5aa63-109">Value</span></span>                                                                        | <span data-ttu-id="5aa63-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5aa63-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5aa63-111"><dt>I</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="5aa63-112">Сообщения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5aa63-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="5aa63-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="5aa63-114">Некритические предупреждения.</span><span class="sxs-lookup"><span data-stu-id="5aa63-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="5aa63-115"><dt>e</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="5aa63-116">Все сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="5aa63-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="5aa63-117"><dt>конкретного</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="5aa63-118">Запуск действий.</span><span class="sxs-lookup"><span data-stu-id="5aa63-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="5aa63-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="5aa63-120">Записи, относящиеся к действию.</span><span class="sxs-lookup"><span data-stu-id="5aa63-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5aa63-121"><dt>u</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="5aa63-122">Запросы пользователей.</span><span class="sxs-lookup"><span data-stu-id="5aa63-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="5aa63-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="5aa63-124">Начальные параметры пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5aa63-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="5aa63-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="5aa63-126">Сведения о нехватке памяти или аварийном завершении.</span><span class="sxs-lookup"><span data-stu-id="5aa63-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="5aa63-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="5aa63-128">Сообщения о нехватке места на диске.</span><span class="sxs-lookup"><span data-stu-id="5aa63-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="5aa63-129"><dt>ш</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="5aa63-130">Свойства терминала.</span><span class="sxs-lookup"><span data-stu-id="5aa63-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="5aa63-131"><dt>3,3</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="5aa63-132">Подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="5aa63-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="5aa63-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="5aa63-134">Дополнительные отладочные сведения.</span><span class="sxs-lookup"><span data-stu-id="5aa63-134">Extra debugging information.</span></span> <span data-ttu-id="5aa63-135">Доступно только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5aa63-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="5aa63-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="5aa63-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="5aa63-137">Запись каждой строки в журнал.</span><span class="sxs-lookup"><span data-stu-id="5aa63-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="5aa63-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5aa63-138">Remarks</span></span>

<span data-ttu-id="5aa63-139">Это свойство доступно начиная с установщик Windows 4,0.</span><span class="sxs-lookup"><span data-stu-id="5aa63-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="5aa63-140">Нельзя использовать значения "+" и " \* " параметра/l в значении свойства **мсилоггинг** .</span><span class="sxs-lookup"><span data-stu-id="5aa63-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="5aa63-141">Режим ведения журнала можно задать с помощью политики, параметра командной строки или программно.</span><span class="sxs-lookup"><span data-stu-id="5aa63-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="5aa63-142">Это переопределяет режим ведения журнала по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5aa63-142">This overrides the default logging mode.</span></span> <span data-ttu-id="5aa63-143">Дополнительные сведения о всех методах, доступных для настройки режима ведения журнала, см. в разделе " [нормальное ведение журнала](normal-logging.md) " раздела [установщик Windows Logging](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa63-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="5aa63-144">Если свойство **мсилоггинг** имеется в [таблице свойств](property-table.md), то режим ведения журнала по умолчанию для пакета можно изменить, изменив значение этого свойства с помощью [преобразования базы данных](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="5aa63-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="5aa63-145">Режим ведения журнала по умолчанию нельзя изменить с помощью [пакета исправлений](patch-packages.md) (MSP-файла).</span><span class="sxs-lookup"><span data-stu-id="5aa63-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="5aa63-146">Если свойство **мсилоггинг** задано в [таблице свойств](property-table.md), для всех пользователей компьютера можно указать режим ведения журнала по умолчанию, задав политику [дисаблелоггингфромпаккаже](disableloggingfrompackage.md) и политику [ведения журнала](logging.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa63-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="5aa63-147">Настройка политики Дисаблелоггингфромпаккаже и политики ведения журнала приведет к переопределению свойства **мсилоггинг** для всех пакетов.</span><span class="sxs-lookup"><span data-stu-id="5aa63-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa63-148">Требования</span><span class="sxs-lookup"><span data-stu-id="5aa63-148">Requirements</span></span>



| <span data-ttu-id="5aa63-149">Требование</span><span class="sxs-lookup"><span data-stu-id="5aa63-149">Requirement</span></span> | <span data-ttu-id="5aa63-150">Значение</span><span class="sxs-lookup"><span data-stu-id="5aa63-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa63-151">Версия</span><span class="sxs-lookup"><span data-stu-id="5aa63-151">Version</span></span><br/> | <span data-ttu-id="5aa63-152">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5aa63-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5aa63-153">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5aa63-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5aa63-154">Установщик Windows 4,5 в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5aa63-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5aa63-155">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa63-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5aa63-156">См. также</span><span class="sxs-lookup"><span data-stu-id="5aa63-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa63-157">Свойства</span><span class="sxs-lookup"><span data-stu-id="5aa63-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5aa63-158">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="5aa63-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 





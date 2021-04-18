---
title: Включение журнала
description: Включение журнала
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Диспетчер устройств Windows Media, ведение журнала
- Диспетчер устройств, ведение журнала
- Классические приложения, ведение журнала
- поставщики услуг, ведение журнала
- инструкции по программированию, ведение журнала
- Ведение журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691179"
---
# <a name="enabling-logging"></a><span data-ttu-id="f89aa-109">Включение журнала</span><span class="sxs-lookup"><span data-stu-id="f89aa-109">Enabling Logging</span></span>

<span data-ttu-id="f89aa-110">Диспетчер устройств Windows Media предоставляет объект ведения журнала, который может сохранять информацию в текстовый файл во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f89aa-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="f89aa-111">Разработчики как приложений, так и поставщиков служб могут использовать этот объект для хранения сообщений в файле журнала во время работы поставщика приложения или службы.</span><span class="sxs-lookup"><span data-stu-id="f89aa-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="f89aa-112">Этот объект особенно полезен при обработке защищенных DRM файлов, так как Windows Media диспетчер устройств не позволяет подключать отладчик к процессу, который обрабатывает файлы, защищенные с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="f89aa-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="f89aa-113">Средство ведения журнала — это COM-объект с ИДЕНТИФИКАТОРом класса CLSID \_ вмдмлогжер, который предоставляет один интерфейс, [**ивмдмлогжер**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="f89aa-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="f89aa-114">Компонентам не требуется сертификат для использования объекта ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f89aa-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="f89aa-115">По умолчанию Windows Media диспетчер устройств поддерживает файл журнала независимо от того, использует ли приложение **ивмдмлогжер**.</span><span class="sxs-lookup"><span data-stu-id="f89aa-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="f89aa-116">Этот файл журнала является простым текстовым файлом, а каждая запись содержит запись, предшествующую метке времени в формате YYYYMMDDHHMMSS, с использованием 24-часового местного времени.</span><span class="sxs-lookup"><span data-stu-id="f89aa-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="f89aa-117">Диспетчер устройств Windows Media записывает все вызовы API, а также все записи, которые добавляются путем вызова сообщений **ивмдмлогжер** .</span><span class="sxs-lookup"><span data-stu-id="f89aa-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="f89aa-118">Все записи файла журнала добавляются к файлу до тех пор, пока не будет вызван [**Сброс**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) или размер файла превышает максимальный.</span><span class="sxs-lookup"><span data-stu-id="f89aa-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="f89aa-119">Файл закрывается автоматически после каждой операции ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f89aa-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="f89aa-120">Для записей приложений и системных записей используется один и тот же файл журнала.</span><span class="sxs-lookup"><span data-stu-id="f89aa-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="f89aa-121">Ниже показано, как использовать объект ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f89aa-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="f89aa-122">Включите вмдмлог. h в проект.</span><span class="sxs-lookup"><span data-stu-id="f89aa-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="f89aa-123">Создайте объект ведения журнала, вызвав **CoCreateInstance**(CLSID \_ вмдмлогжер) и запрашивая интерфейс **ивмдмлогжер** .</span><span class="sxs-lookup"><span data-stu-id="f89aa-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="f89aa-124">Назначьте указатель интерфейса глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="f89aa-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="f89aa-125">Убедитесь, что ведение журнала включено, вызвав [**ивмдмлогжер:: enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Если это не так, включите его, вызвав [**ивмдмлогжер:: enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span><span class="sxs-lookup"><span data-stu-id="f89aa-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="f89aa-126">Укажите имя и размер настраиваемого файла журнала.</span><span class="sxs-lookup"><span data-stu-id="f89aa-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="f89aa-127">Это делается путем вызова [**ивмдмлогжер:: сетлогфиленаме**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) и [**Ивмдмлогжер:: сетсизепарамс**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span><span class="sxs-lookup"><span data-stu-id="f89aa-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="f89aa-128">В точках кода, где необходимо создать запись в журнале, вызовите [**ивмдмлогжер:: логдворд**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) для строк журнала, содержащих переменные (этот метод похож на **вспринтф** , так как он позволяет отформатировать строку, содержащую значение переменной), или вызвать [**ивмдмлогжер:: логстринг**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) для записи в журнал строк констант.</span><span class="sxs-lookup"><span data-stu-id="f89aa-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="f89aa-129">Пример кода см. на страницах справочника по методам [**ивмдмлогжер**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="f89aa-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f89aa-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f89aa-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f89aa-131">**Задачи, общие для приложений и поставщиков служб**</span><span class="sxs-lookup"><span data-stu-id="f89aa-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





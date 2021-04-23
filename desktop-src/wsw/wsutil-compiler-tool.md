---
title: Средство компилятора Всутил
description: Средство компилятора веб-служб Windows, WsUtil.exe, поддерживает модель службы и сериализацию типов данных. Он обрабатывает WSDL, схему XML и документы политик, а также создает заголовки C и исходные файлы.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Веб-службы средства компилятора Всутил для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988004"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="4fc17-107">Средство компилятора Всутил</span><span class="sxs-lookup"><span data-stu-id="4fc17-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="4fc17-108">Средство компилятора веб-служб Windows, WsUtil.exe, поддерживает [модель службы](service-model-layer-overview.md) и [сериализацию](serialization.md) типов данных.</span><span class="sxs-lookup"><span data-stu-id="4fc17-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="4fc17-109">Он обрабатывает WSDL, схему XML и документы политик, а также создает заголовки C и исходные файлы.</span><span class="sxs-lookup"><span data-stu-id="4fc17-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="4fc17-110">Это средство аналогично средству компилятора WSDL для управляемого кода, но предназначено для машинного кода.</span><span class="sxs-lookup"><span data-stu-id="4fc17-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="4fc17-111">Для поддержки [модели службы](service-model-layer-overview.md)WsUtil.exe создает заголовки, которые будут использоваться как для клиента, так и для службы.</span><span class="sxs-lookup"><span data-stu-id="4fc17-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="4fc17-112">Он создает прокси-файл C для стороны клиента и файлы заглушки C для стороны службы, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="4fc17-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="4fc17-113">Для поддержки [сериализации](serialization.md)компилятор создает заголовки для описаний элементов для определений глобальных элементов и все сведения об определении типа в прокси-файлах, которые используются ядром сериализации.</span><span class="sxs-lookup"><span data-stu-id="4fc17-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="4fc17-114">Параметры командной строки для обработки WSDL-файлов, файлов схем XML и файлов политик веб-службы см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="4fc17-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="4fc17-115">Средство компилятора веб-служб</span><span class="sxs-lookup"><span data-stu-id="4fc17-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="4fc17-116">WSDL и контракты служб</span><span class="sxs-lookup"><span data-stu-id="4fc17-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="4fc17-117">Поддержка схем</span><span class="sxs-lookup"><span data-stu-id="4fc17-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="4fc17-118">Поддержка политик</span><span class="sxs-lookup"><span data-stu-id="4fc17-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="4fc17-119">Безопасность</span><span class="sxs-lookup"><span data-stu-id="4fc17-119">Security</span></span>

<span data-ttu-id="4fc17-120">При использовании Всутил учитывайте следующие проблемы и следите за соответствующими мерами.</span><span class="sxs-lookup"><span data-stu-id="4fc17-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="4fc17-121">Всутил не получает XML-метаданные по сети, а всутил не разрешает инструкции import и/или include во входных файлах метаданных.</span><span class="sxs-lookup"><span data-stu-id="4fc17-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="4fc17-122">Всутил открывает и считывает файлы WSDL, XSD и политики.</span><span class="sxs-lookup"><span data-stu-id="4fc17-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="4fc17-123">Метаданные XML не защищены от несанкционированного изменения.</span><span class="sxs-lookup"><span data-stu-id="4fc17-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="4fc17-124">Убедитесь, что вы используете только файлы WSDL, XSD и политики, полученные из надежного источника, и убедитесь, что они защищены от несанкционированного изменения до и после их использования.</span><span class="sxs-lookup"><span data-stu-id="4fc17-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="4fc17-125">Внимательно проверьте содержимое входных файлов и убедитесь, что содержимое файлов надежно для использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="4fc17-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="4fc17-126">Wsutil.exe не выполняет проверку подлинности файлов метаданных.</span><span class="sxs-lookup"><span data-stu-id="4fc17-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="4fc17-127">Всутил создает файлы заголовка и заглушки, которые не защищены от изменения.</span><span class="sxs-lookup"><span data-stu-id="4fc17-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="4fc17-128">Необходимо установить правильные права доступа на уровне исходных файлов, созданных wsutil.exe, чтобы запретить унаусоритизед доступ к этим файлам.</span><span class="sxs-lookup"><span data-stu-id="4fc17-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="4fc17-129">Всутил использует System. IO. StreamWriter для создания выходных файлов.</span><span class="sxs-lookup"><span data-stu-id="4fc17-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="4fc17-130">Пользователи должны иметь в виду, что Всутил может перезаписать свои локальные файлы, и следует осторожно указывать имена файлов и каталоги для выходных файлов с помощью параметра/out.</span><span class="sxs-lookup"><span data-stu-id="4fc17-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="4fc17-131">Всутил или wsutilhelper.dll, загруженные в wsutil.exe, могут неожиданно завершить работу или потреблять большой объем системных ресурсов при атаке или обработке очень большого количества входных метаданных.</span><span class="sxs-lookup"><span data-stu-id="4fc17-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="4fc17-132">Это средство предназначено для использования во время разработки. только это средство следует использовать только в качестве средства времени разработки.</span><span class="sxs-lookup"><span data-stu-id="4fc17-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="4fc17-133">Использование на среднем уровне для обработки сведений о политике может быть ненадежным.</span><span class="sxs-lookup"><span data-stu-id="4fc17-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="4fc17-134">Библиотека DLL модуля поддержки Wsutilhelper.dll загружается в управляемые wsutil.exe для обработки сведений о политике.</span><span class="sxs-lookup"><span data-stu-id="4fc17-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="4fc17-135">Пользователь должен убедиться в том, что в пути к двоичному файлу не существует вредоносного двоичного файла с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="4fc17-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="4fc17-136">Аналогично, пользователь должен убедиться в том, что в среде сборки двоичный путь правильно настроен, что не существует вредоносного двоичного файла с тем же именем "wsutil.exe".</span><span class="sxs-lookup"><span data-stu-id="4fc17-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="4fc17-137">По возможности всутил создает аннотацию SAL для операций и полей структуры.</span><span class="sxs-lookup"><span data-stu-id="4fc17-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="4fc17-138">Пользователь созданных файлов всутил должен соответствовать требованию, указанному в аннотации SAL.</span><span class="sxs-lookup"><span data-stu-id="4fc17-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fc17-139">См. также</span><span class="sxs-lookup"><span data-stu-id="4fc17-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fc17-140">Обзор уровня модели службы</span><span class="sxs-lookup"><span data-stu-id="4fc17-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="4fc17-141">Сериализация</span><span class="sxs-lookup"><span data-stu-id="4fc17-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="4fc17-142">Средство компилятора веб-служб</span><span class="sxs-lookup"><span data-stu-id="4fc17-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="4fc17-143">Поддержка языка WSDL</span><span class="sxs-lookup"><span data-stu-id="4fc17-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="4fc17-144">Поддержка схем</span><span class="sxs-lookup"><span data-stu-id="4fc17-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="4fc17-145">Поддержка политик</span><span class="sxs-lookup"><span data-stu-id="4fc17-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 





---
description: Описывает входные файлы, используемые Всдкодежен, и выходные файлы, созданные Всдкодежен.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: О Всдкодежен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080582"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="f4f69-103">О Всдкодежен</span><span class="sxs-lookup"><span data-stu-id="f4f69-103">About WsdCodeGen</span></span>

<span data-ttu-id="f4f69-104">Всдкодежен использует XML-файл конфигурации для определения расположения метаданных службы.</span><span class="sxs-lookup"><span data-stu-id="f4f69-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="f4f69-105">Файл конфигурации также используется для определения имен интерфейсов, идентификаторов GUID интерфейса, имен классов, имен методов и других идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="f4f69-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="f4f69-106">Дополнительные сведения об этом файле см. в разделе [Всдкодежен Configuration File](wsdcodegen-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="f4f69-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="f4f69-107">Всдкодежен требует наличия двух типов входных файлов: XML-файла конфигурации и одного или нескольких файлов описания службы (WSDL и/или XSD-файлы).</span><span class="sxs-lookup"><span data-stu-id="f4f69-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="f4f69-108">Всдкодежен обрабатывает эти входные файлы и формирует два типа выходных файлов: файлы интерфейсов и файлы заголовков и исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="f4f69-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="f4f69-109">Входные файлы</span><span class="sxs-lookup"><span data-stu-id="f4f69-109">Input Files</span></span>



| <span data-ttu-id="f4f69-110">Тип</span><span class="sxs-lookup"><span data-stu-id="f4f69-110">Type</span></span>                      | <span data-ttu-id="f4f69-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f4f69-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f69-112">Файл конфигурации</span><span class="sxs-lookup"><span data-stu-id="f4f69-112">Configuration file</span></span>        | <span data-ttu-id="f4f69-113">XML-файл, который указывает расположение метаданных службы и определяет имена интерфейсов, идентификаторы GUID интерфейса, имена классов, имена методов и другие идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="f4f69-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="f4f69-114">Файлы описания службы</span><span class="sxs-lookup"><span data-stu-id="f4f69-114">Service description files</span></span> | <span data-ttu-id="f4f69-115">Один или несколько файлов WSDL или XSD, описывающих службы, которые должны быть реализованы на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f4f69-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="f4f69-116">Выходные файлы</span><span class="sxs-lookup"><span data-stu-id="f4f69-116">Output Files</span></span>



| <span data-ttu-id="f4f69-117">Тип</span><span class="sxs-lookup"><span data-stu-id="f4f69-117">Type</span></span>                        | <span data-ttu-id="f4f69-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f4f69-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f69-119">Файлы интерфейса</span><span class="sxs-lookup"><span data-stu-id="f4f69-119">Interface files</span></span>             | <span data-ttu-id="f4f69-120">Файл IDL (язык определения интерфейса), который можно использовать с компилятором MIDL для создания файла заголовка интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f4f69-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="f4f69-121">Для использования этого файла интерфейса WSDAPI клиенты и службы WSDAPI могут использовать этот файл.</span><span class="sxs-lookup"><span data-stu-id="f4f69-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="f4f69-122">Файлы заголовков и исходных файлов C++</span><span class="sxs-lookup"><span data-stu-id="f4f69-122">C++ header and source files</span></span> | <span data-ttu-id="f4f69-123">Файлы C++, описывающие контракт сообщения, пространство имен и сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="f4f69-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="f4f69-124">Они могут содержать код прокси-сервера и/или код заглушки.</span><span class="sxs-lookup"><span data-stu-id="f4f69-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="f4f69-125">Код прокси-сервера реализует интерфейс службы и преобразует вызовы метода службы в операции WSDAPI, которые делают запросы на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f4f69-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="f4f69-126">Код заглушки преобразует запросы службы WSDAPI в код, вызывающий методы службы.</span><span class="sxs-lookup"><span data-stu-id="f4f69-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f4f69-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f4f69-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4f69-128">Генератор кода для веб-служб на устройствах</span><span class="sxs-lookup"><span data-stu-id="f4f69-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="f4f69-129">Использование Всдкодежен</span><span class="sxs-lookup"><span data-stu-id="f4f69-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




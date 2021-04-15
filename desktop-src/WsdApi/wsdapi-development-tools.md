---
description: Средства разработки WSDAPI, включенные в Windows SDK (WSD CodeGen, узел отладки WSD и клиент отладки WSD), позволяют разработчикам создавать и отлаживать клиенты и устройства на основе WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Средства разработки WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701931"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="d2709-103">Средства разработки WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d2709-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="d2709-104">Средства разработки WSDAPI, включенные в Windows SDK (WSD CodeGen, узел отладки WSD и клиент отладки WSD), позволяют разработчикам создавать и отлаживать клиенты и устройства на основе WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="d2709-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="d2709-105">Исходный код для этих средств недоступен.</span><span class="sxs-lookup"><span data-stu-id="d2709-105">The source code for these tools is not available.</span></span> <span data-ttu-id="d2709-106">Средства пакета SDK находятся в следующем каталоге: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="d2709-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="d2709-107">WSD CodeGen (wsdcodegen.exe) преобразует контракт WSDL в созданный код C++, который разработчики могут вызывать напрямую в.</span><span class="sxs-lookup"><span data-stu-id="d2709-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="d2709-108">Он обрабатывает представление сериализации данных и подключения, чтобы разработчики могли сосредоточиться на проектировании приложений.</span><span class="sxs-lookup"><span data-stu-id="d2709-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="d2709-109">Дополнительные сведения о CodeGenе WSD см. [в разделе веб-службы на устройствах генератор кода](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="d2709-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="d2709-110">Это средство доступно в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows и в комплекте драйверов для Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="d2709-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="d2709-111">Средства отладки сервера WSD (всддебуг \_host.exe) и клиент отладки WSD (всддебуг \_client.exe) помогают разработчикам в отладке своих клиентов и узлов.</span><span class="sxs-lookup"><span data-stu-id="d2709-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="d2709-112">Эти средства можно использовать для проверки и проверки WS-Discovery и трафика обмена метаданными.</span><span class="sxs-lookup"><span data-stu-id="d2709-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="d2709-113">Дополнительные сведения об узле отладки WSD и клиенте отладки WSD см. в разделе [средства отладки](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d2709-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="d2709-114">Эти средства доступны только в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d2709-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="d2709-115">Существует дополнительное средство разработки с именем " [основной инструмент взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx)", которое доступно только в WDK.</span><span class="sxs-lookup"><span data-stu-id="d2709-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="d2709-116">Это средство используется для тестирования методов служб, механизма оптимизации передачи сообщений (MTOM), вложений или WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="d2709-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2709-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d2709-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2709-118">Разработка приложений WSD в Windows</span><span class="sxs-lookup"><span data-stu-id="d2709-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="d2709-119">Генератор кода для веб-служб на устройствах</span><span class="sxs-lookup"><span data-stu-id="d2709-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="d2709-120">Базовое средство взаимодействия WSDAPI (ВСДБИТ)</span><span class="sxs-lookup"><span data-stu-id="d2709-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="d2709-121">Средства отладки</span><span class="sxs-lookup"><span data-stu-id="d2709-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 




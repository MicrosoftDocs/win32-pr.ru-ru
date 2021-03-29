---
description: Расширенные примеры Winsock с использованием расширений SSL
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Расширенные примеры Winsock с использованием расширений SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991118"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="a0326-103">Расширенные примеры Winsock с использованием расширений SSL</span><span class="sxs-lookup"><span data-stu-id="a0326-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="a0326-104">Пример защиты клиента и сервера TCP</span><span class="sxs-lookup"><span data-stu-id="a0326-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="a0326-105">Более сложный пример Winsock, демонстрирующий использование расширений SSL, входит в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a0326-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a0326-106">Этот пример включает клиент TCP и сервер, которые безопасно подключаются с помощью Winsock и расширений SSL.</span><span class="sxs-lookup"><span data-stu-id="a0326-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="a0326-107">По умолчанию исходный код примера Winsock устанавливается в следующий каталог:</span><span class="sxs-lookup"><span data-stu-id="a0326-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="a0326-108">*C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ нетдс \\ Winsock*</span><span class="sxs-lookup"><span data-stu-id="a0326-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="a0326-109">Пример находится в следующей папке:</span><span class="sxs-lookup"><span data-stu-id="a0326-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="a0326-110">*секуресоккет*</span><span class="sxs-lookup"><span data-stu-id="a0326-110">*securesocket*</span></span>

<span data-ttu-id="a0326-111">Пример кода разбивается на отдельные каталоги, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="a0326-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="a0326-112">сткпклиент — папка, содержащая код защищенного клиента TCP.</span><span class="sxs-lookup"><span data-stu-id="a0326-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="a0326-113">сткпкоммон — папка, содержащая общий код библиотеки, который является общим для защищенного клиента TCP и сервера.</span><span class="sxs-lookup"><span data-stu-id="a0326-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="a0326-114">сткпсервер — папка, содержащая код защищенного TCP-сервера.</span><span class="sxs-lookup"><span data-stu-id="a0326-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="a0326-115">Следует отметить, что образцы предназначены для запуска на двух разных компьютерах под управлением Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a0326-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="a0326-116">Кроме того, учетные данные IPsec должны быть подготовлены на обоих компьютерах для обеспечения успешности подключения, поскольку в примере используется протокол IPsec для защиты своего трафика.</span><span class="sxs-lookup"><span data-stu-id="a0326-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="a0326-117">Дополнительные сведения о настройке учетных данных IPsec см. в документации по [конфигурации IPSec](/windows/desktop/FWP/ipsec-configuration) .</span><span class="sxs-lookup"><span data-stu-id="a0326-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="a0326-118">При построении образца будут созданы два исполняемых файла:</span><span class="sxs-lookup"><span data-stu-id="a0326-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="a0326-119">*stcpclient.exe* и *stcpserver.exe*.</span><span class="sxs-lookup"><span data-stu-id="a0326-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="a0326-120">Скопируйте *stcpclient.exe* на компьютер A и скопируйте *stcpserver.exe* на компьютер B. На компьютере B запустите TCP-сервер, выполнив в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a0326-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="a0326-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="a0326-121">**stcpserver.exe**</span></span>

<span data-ttu-id="a0326-122">Чтобы получить дополнительные параметры использования для сервера, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a0326-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="a0326-123">**stcpserver.exe/?**</span><span class="sxs-lookup"><span data-stu-id="a0326-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="a0326-124">Затем на компьютере а запустите TCP-клиент, выполнив в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a0326-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="a0326-125">**stcpclient.exe <полное DNS-имя-для-Machine-B>**</span><span class="sxs-lookup"><span data-stu-id="a0326-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="a0326-126">На этом этапе подключение должно быть установлено безопасно.</span><span class="sxs-lookup"><span data-stu-id="a0326-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="a0326-127">Чтобы получить дополнительные параметры использования для клиента, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a0326-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="a0326-128">**stcpclient.exe/?**</span><span class="sxs-lookup"><span data-stu-id="a0326-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0326-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a0326-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0326-130">О платформе фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="a0326-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="a0326-131">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="a0326-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="a0326-132">Конфигурация IPsec</span><span class="sxs-lookup"><span data-stu-id="a0326-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="a0326-133">Функции IPsec</span><span class="sxs-lookup"><span data-stu-id="a0326-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="a0326-134">Использование расширений SSL</span><span class="sxs-lookup"><span data-stu-id="a0326-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="a0326-135">интерфейс поставщика поддержки безопасности (SSPI)</span><span class="sxs-lookup"><span data-stu-id="a0326-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="a0326-136">Платформа фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="a0326-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="a0326-137">Функции API платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="a0326-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="a0326-138">Расширения безопасных сокетов Winsock</span><span class="sxs-lookup"><span data-stu-id="a0326-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 

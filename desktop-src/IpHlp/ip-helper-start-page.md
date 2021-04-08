---
description: API вспомогательного приложения протокола Интернета (IP-адрес) обеспечивает извлечение и изменение параметров конфигурации сети для локального компьютера.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Вспомогательная служба IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897214"
---
# <a name="ip-helper"></a><span data-ttu-id="1a6b7-103">Вспомогательная служба IP</span><span class="sxs-lookup"><span data-stu-id="1a6b7-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="1a6b7-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="1a6b7-104">Purpose</span></span>

<span data-ttu-id="1a6b7-105">API вспомогательного приложения протокола Интернета (IP-адрес) обеспечивает извлечение и изменение параметров конфигурации сети для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1a6b7-106">Где применимо</span><span class="sxs-lookup"><span data-stu-id="1a6b7-106">Where applicable</span></span>

<span data-ttu-id="1a6b7-107">API вспомогательной функции IP применим в любой вычислительной среде, где программно манипулировать сетью и конфигурацией TCP/IP очень удобно.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="1a6b7-108">Типичные приложения включают протоколы IP-маршрутизации и агенты SNMP.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1a6b7-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="1a6b7-109">Developer audience</span></span>

<span data-ttu-id="1a6b7-110">API вспомогательной функции IP предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="1a6b7-111">Программисты также должны быть знакомы с основными понятиями сетей Windows и TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1a6b7-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="1a6b7-112">Run-time requirements</span></span>

<span data-ttu-id="1a6b7-113">API вспомогательной функции IP можно использовать на всех платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="1a6b7-114">Не все операционные системы поддерживают все функции.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="1a6b7-115">Если существуют определенные реализации или возможности ограничений платформы Windows Sockets 2, они четко отмечены в документации.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="1a6b7-116">Если вспомогательная функция IP вызывается на платформе, которая не поддерживает эту функцию, возвращается ошибка \_ не \_ поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="1a6b7-117">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделах о требованиях в документации.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a6b7-118">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1a6b7-118">In this section</span></span>



| <span data-ttu-id="1a6b7-119">Раздел</span><span class="sxs-lookup"><span data-stu-id="1a6b7-119">Topic</span></span>                                                              | <span data-ttu-id="1a6b7-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1a6b7-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a6b7-121">Новые возможности вспомогательного приложения IP</span><span class="sxs-lookup"><span data-stu-id="1a6b7-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="1a6b7-122">Сведения о новых возможностях для поддержки IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="1a6b7-123">Сведения о вспомогательном модуле IP</span><span class="sxs-lookup"><span data-stu-id="1a6b7-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="1a6b7-124">Общие сведения о требованиях к программированию вспомогательного программного обеспечения и возможностях, доступных разработчикам.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="1a6b7-125">Использование вспомогательного метода IP</span><span class="sxs-lookup"><span data-stu-id="1a6b7-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="1a6b7-126">Процедуры и методы программирования, используемые с вспомогательным модулем IP.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="1a6b7-127">В этом разделе приводятся основные методы программирования вспомогательных программ для IP-адресов, например [Начало работы с помощью вспомогательного метода IP](getting-started-with-ip-helper.md).</span><span class="sxs-lookup"><span data-stu-id="1a6b7-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="1a6b7-128">Справочные материалы по IP Helper</span><span class="sxs-lookup"><span data-stu-id="1a6b7-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="1a6b7-129">Справочная документация по вспомогательным функциям, структурам и перечислениям IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="1a6b7-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="1a6b7-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1a6b7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6b7-131">Сокеты Windows 2</span><span class="sxs-lookup"><span data-stu-id="1a6b7-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="1a6b7-132">Служба маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="1a6b7-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 


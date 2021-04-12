---
title: Удаленный доступ
description: Используйте службу удаленного доступа (RAS) для создания клиентских приложений.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS службы удаленного доступа
- RAS RAS
- RAS-сервер службы удаленного доступа, начальная страница
- RAS, см. раздел удаленный доступ.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104133531"
---
# <a name="remote-access"></a><span data-ttu-id="0cb93-107">Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="0cb93-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="0cb93-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="0cb93-108">Purpose</span></span>

<span data-ttu-id="0cb93-109">Используйте службу удаленного доступа (RAS) для создания клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="0cb93-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="0cb93-110">В этих приложениях отображаются общие диалоговые окна службы RAS, Управление подключениями и устройствами удаленного доступа и работа с записями в телефонной книге.</span><span class="sxs-lookup"><span data-stu-id="0cb93-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="0cb93-111">Служба RAS также обеспечивает следующее поколение серверной функциональности для службы удаленного доступа (RAS) для Windows.</span><span class="sxs-lookup"><span data-stu-id="0cb93-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="0cb93-112">Функции сервера RRAS следуют и создаются на основе службы удаленного доступа (RAS).</span><span class="sxs-lookup"><span data-stu-id="0cb93-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="0cb93-113">Где применимо</span><span class="sxs-lookup"><span data-stu-id="0cb93-113">Where applicable</span></span>

<span data-ttu-id="0cb93-114">Служба удаленного доступа применима в любой вычислительной среде, которая использует ссылку на глобальную сеть (WAN) или виртуальную частную сеть (VPN).</span><span class="sxs-lookup"><span data-stu-id="0cb93-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="0cb93-115">Служба RAS позволяет подключать удаленный клиентский компьютер к сетевому серверу по каналу WAN или VPN.</span><span class="sxs-lookup"><span data-stu-id="0cb93-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="0cb93-116">Затем удаленный компьютер работает в локальной сети сервера, как будто удаленный компьютер подключен к локальной сети напрямую.</span><span class="sxs-lookup"><span data-stu-id="0cb93-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="0cb93-117">API RAS позволяет программистам получать доступ к функциям RAS программным способом.</span><span class="sxs-lookup"><span data-stu-id="0cb93-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="0cb93-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="0cb93-118">Developer audience</span></span>

<span data-ttu-id="0cb93-119">API службы RAS предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="0cb93-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="0cb93-120">Программисты Microsoft Visual Basic также могут найти полезные API.</span><span class="sxs-lookup"><span data-stu-id="0cb93-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="0cb93-121">Программисты должны быть знакомы с основными понятиями сети.</span><span class="sxs-lookup"><span data-stu-id="0cb93-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="0cb93-122">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="0cb93-122">Run-time requirements</span></span>

<span data-ttu-id="0cb93-123">Некоторые функции в API RAS поддерживаются только на сетевых серверах, и другие функции поддерживаются только для сетевых клиентов.</span><span class="sxs-lookup"><span data-stu-id="0cb93-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="0cb93-124">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделах о требованиях в документации.</span><span class="sxs-lookup"><span data-stu-id="0cb93-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="0cb93-125">[Усовершенствованная функциональность службы удаленного доступа](function-comparison-windows-2000-versus-rras-redistributable.md) к RRAS доступна для Windows NT Server 4,0 путем установки [распространяемого компонента RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span><span class="sxs-lookup"><span data-stu-id="0cb93-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="0cb93-126">Все функции службы RRAS включены в Windows 2000 Server, Windows Server 2003 и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0cb93-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="0cb93-127">Приложения RRAS не могут работать на компьютерах под управлением Windows NT Workstation 4,0 или в клиентских операционных системах, таких как Windows 95.</span><span class="sxs-lookup"><span data-stu-id="0cb93-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="0cb93-128">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделах о требованиях в документации.</span><span class="sxs-lookup"><span data-stu-id="0cb93-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0cb93-129">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="0cb93-129">In this section</span></span>



| <span data-ttu-id="0cb93-130">Раздел</span><span class="sxs-lookup"><span data-stu-id="0cb93-130">Topic</span></span>                                                                                             | <span data-ttu-id="0cb93-131">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb93-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cb93-132">Служба удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="0cb93-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="0cb93-133">Служба удаленного доступа (RAS) предоставляет возможности удаленного доступа к клиентским приложениям на компьютерах под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="0cb93-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="0cb93-134">Администрирование службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="0cb93-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="0cb93-135">Администрирование службы удаленного доступа предоставляет набор функций для администрирования разрешений пользователей и портов на серверах RAS.</span><span class="sxs-lookup"><span data-stu-id="0cb93-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="0cb93-136">С помощью этих функций можно разработать приложение для администрирования сервера удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="0cb93-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0cb93-137">См. также</span><span class="sxs-lookup"><span data-stu-id="0cb93-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cb93-138">Маршрутизация</span><span class="sxs-lookup"><span data-stu-id="0cb93-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="0cb93-139">Протоколы маршрутизации</span><span class="sxs-lookup"><span data-stu-id="0cb93-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 






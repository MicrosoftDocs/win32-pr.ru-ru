---
title: Платформа датчика
description: Windows 7 изменила принципы использования датчиков разработчиками.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070241"
---
# <a name="sensor-platform"></a><span data-ttu-id="c5efb-103">Платформа датчика</span><span class="sxs-lookup"><span data-stu-id="c5efb-103">Sensor Platform</span></span>

<span data-ttu-id="c5efb-104">Windows 7 изменила принципы использования датчиков разработчиками.</span><span class="sxs-lookup"><span data-stu-id="c5efb-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="c5efb-105">Она включает встроенную поддержку датчиков, которая расширяется новой платформой разработки для работы с датчиками, включая датчики расположения, такие как устройства GPS (Global Position Systems).</span><span class="sxs-lookup"><span data-stu-id="c5efb-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="c5efb-106">Интерфейсы API *расположения Windows*, созданные на платформе датчиков, — это новая функция Windows 7, позволяющая разработчикам приложений получать доступ к сведениям о физическом расположении пользователя.</span><span class="sxs-lookup"><span data-stu-id="c5efb-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="c5efb-107">Интерфейсы API *расположения Windows* могут быть абстрактным оборудованием, одновременно поддерживать несколько приложений и легко переключаться между различными технологиями, освобождая разработчика разработчику приложений о затратах на управление этими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="c5efb-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="c5efb-108">Программисты могут использовать интерфейсы API *расположения*, используя язык программирования C++ (программисты, знакомые с моделью COM) или объекты COM в языках сценариев, таких как Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="c5efb-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="c5efb-109">Поддержка сценариев обеспечивает простой доступ к данным о расположении для таких проектов, как мини-приложения.</span><span class="sxs-lookup"><span data-stu-id="c5efb-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="c5efb-110">Windows 7 предоставляет надежную, простую в использовании платформу для использования сенсорных устройств, таких как внешний датчик освещения или датчик температуры, для создания сведений о среде в приложениях Windows.</span><span class="sxs-lookup"><span data-stu-id="c5efb-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="c5efb-111">ПК могут использовать датчики, встроенные в компьютер, подключенные через проводные или беспроводные подключения или подключенные по сети или *через Интернет*.</span><span class="sxs-lookup"><span data-stu-id="c5efb-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="c5efb-112">Интерфейсы API *датчиков* и *расположений* предоставляют стандартный способ обнаружения датчиков и программного доступа к данным, предоставляемым датчиками.</span><span class="sxs-lookup"><span data-stu-id="c5efb-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="c5efb-113">Панель управления *датчика* позволяет пользователям включать или отключать датчики, управлять доступом к датчикам, которые могут предоставлять конфиденциальные данные, просматривать свойства датчика и изменять описания датчиков.</span><span class="sxs-lookup"><span data-stu-id="c5efb-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="c5efb-114">[Расширение класса датчика](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) является основной частью модели разработки драйверов для платформы датчиков.</span><span class="sxs-lookup"><span data-stu-id="c5efb-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="c5efb-115">Он предоставляет следующие механизмы, которые используются при написании драйвера датчика [платформы драйверов (UMDF) пользовательского режима](https://developer.microsoft.com/windows/hardware) .</span><span class="sxs-lookup"><span data-stu-id="c5efb-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="c5efb-116">Интеграция с платформой датчика</span><span class="sxs-lookup"><span data-stu-id="c5efb-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="c5efb-117">Обеспечение безопасности</span><span class="sxs-lookup"><span data-stu-id="c5efb-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5efb-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c5efb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5efb-119">API датчика</span><span class="sxs-lookup"><span data-stu-id="c5efb-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>
---
description: Классы устройств упрощают разработку, позволяя программистам обрабатывать устройства с похожими свойствами аналогичным образом.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Класс устройств (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998479"
---
# <a name="device-class"></a><span data-ttu-id="252b1-103">Класс устройства</span><span class="sxs-lookup"><span data-stu-id="252b1-103">Device Class</span></span>

<span data-ttu-id="252b1-104">Классы устройств упрощают разработку, позволяя программистам обрабатывать устройства с похожими свойствами аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="252b1-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="252b1-105">Например, цифровой телефон в офисе, как правило, имеет больше возможностей, чем стандартная телефонная трубка, но оба они отвечают на основной набор функций и оба относятся к классу телефонных устройств.</span><span class="sxs-lookup"><span data-stu-id="252b1-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="252b1-106">Классы устройств помогают сделать TAPI расширяемым, предоставляя платформу для классификации и поддержки нового оборудования.</span><span class="sxs-lookup"><span data-stu-id="252b1-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="252b1-107">Классы, которые интерфейс TAPI предопределен, см. в разделе [классы устройств TAPI](./tapi-device-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="252b1-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="252b1-108">Поставщик услуг может реализовать и определить дополнительные классы устройств для оборудования, которое он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="252b1-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="252b1-109">Приложению никогда не нужно указывать, какой поставщик услуг управляет этим устройством, но может потребовать сведения об управлении новыми классами устройств.</span><span class="sxs-lookup"><span data-stu-id="252b1-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="252b1-110">Поставщик услуг реализует класс устройства путем сопоставления запросов с фактическими командами устройства.</span><span class="sxs-lookup"><span data-stu-id="252b1-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="252b1-111">Например, если поставщик услуг для модема, совместимого с Hayes, получает команду, переданную через ТАПИСВР для вызова, он отправляет модему классические команды AT.</span><span class="sxs-lookup"><span data-stu-id="252b1-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="252b1-112">Интерфейс поставщика услуг может быть сопоставлен с широким спектром сред, включая те, которые обычно не были рассмотрены как принадлежащие телефонии.</span><span class="sxs-lookup"><span data-stu-id="252b1-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="252b1-113">Примером может служить мультимедиа-конференцию в сети на основе IP, например в Интернете.</span><span class="sxs-lookup"><span data-stu-id="252b1-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="252b1-114">Разработчикам приложений следует помнить о существовании других приложений, которые могут совместно использовать службы телефонии.</span><span class="sxs-lookup"><span data-stu-id="252b1-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 

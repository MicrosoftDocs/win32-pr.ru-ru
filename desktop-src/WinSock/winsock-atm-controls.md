---
description: Установка и уничтожение подключений "точка — точка" и "точка — MultiPoint" изначально поддерживается спецификацией Windows Sockets 2.
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Элементы управления Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3eb0fc798878066f6e3a4fa04af688eee28ea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711009"
---
# <a name="winsock-atm-controls"></a><span data-ttu-id="f4a22-103">Элементы управления Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="f4a22-103">Winsock ATM Controls</span></span>

<span data-ttu-id="f4a22-104">Установка и уничтожение подключений "точка — точка" и "точка — MultiPoint" изначально поддерживается спецификацией Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="f4a22-104">ATM point-to-point and point-to-multipoint connection setup and teardown are natively supported by the Windows Sockets 2 specification.</span></span> <span data-ttu-id="f4a22-105">Фактически Спецификация качества обслуживания Windows Sockets 2 и независимые от протокола механизмы MultiPoint и многоадресной рассылки разрабатывались с учетом БАНКОМАТов вместе с другими протоколами.</span><span class="sxs-lookup"><span data-stu-id="f4a22-105">In fact, Windows Sockets 2 QoS specification and protocol-independent multipoint/multicast mechanisms were designed with ATM in mind, along with other protocols.</span></span> <span data-ttu-id="f4a22-106">См. раздел 2,7 и приложение D спецификации API Windows Sockets 2 для Windows Sockets 2, качества обслуживания и поддержки MultiPoint соответственно.</span><span class="sxs-lookup"><span data-stu-id="f4a22-106">See Section 2.7 and Appendix D of the Windows Sockets 2 API specification for Windows Sockets 2, Quality of Service, and Multipoint Support, respectively.</span></span> <span data-ttu-id="f4a22-107">Поэтому в этом документе не нужно вводить запросы ioctl, относящиеся к ATM.</span><span class="sxs-lookup"><span data-stu-id="f4a22-107">Therefore, no ATM-specific Ioctls need to be introduced in this document.</span></span>

 

 




---
description: Параметры SSPI для распределенных приложений
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Параметры SSPI для распределенных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896650"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="979cd-103">Параметры SSPI для распределенных приложений</span><span class="sxs-lookup"><span data-stu-id="979cd-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="979cd-104">У разработчиков есть множество вариантов создания распределенных приложений.</span><span class="sxs-lookup"><span data-stu-id="979cd-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="979cd-105">[*Интерфейс поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI) обеспечивает уровень абстракции между протоколами уровня приложения и [*протоколами безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="979cd-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="979cd-106">Приложения могут использовать преимущества протоколов безопасности SSPI несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="979cd-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="979cd-107">Напрямую вызывайте подпрограммы SSPI (для традиционных приложений на основе сокетов).</span><span class="sxs-lookup"><span data-stu-id="979cd-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="979cd-108">Для реализации [*протокола приложения*](../secgloss/a-gly.md) , который передает данные, связанные с безопасностью SSPI, подпрограммы используют сообщения "запрос-ответ".</span><span class="sxs-lookup"><span data-stu-id="979cd-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="979cd-109">Используйте COM для вызова параметров безопасности, реализованных с помощью проверки подлинности RPC и SSPI на более низких уровнях.</span><span class="sxs-lookup"><span data-stu-id="979cd-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="979cd-110">Эти приложения не вызывают функции SSPI напрямую.</span><span class="sxs-lookup"><span data-stu-id="979cd-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="979cd-111">Используйте [сокеты Windows 2](../winsock/windows-sockets-start-page-2.md) (Winsock) с расширенным интерфейсом Winsock, чтобы предоставить поставщикам транспорта возможность использовать функции безопасности.</span><span class="sxs-lookup"><span data-stu-id="979cd-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="979cd-112">Этот подход интегрирует [*поставщик поддержки безопасности*](../secgloss/s-gly.md) (SSP) в сетевой стек и предоставляет службы безопасности и транспорта через общий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="979cd-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="979cd-113">Используйте [API расширений Интернета Windows](../wininet/portal.md) (WinInet) и интерфейс, предназначенный для поддержки протоколов безопасности Интернета, таких как протокол [*SSL*](../secgloss/s-gly.md) (SSL).</span><span class="sxs-lookup"><span data-stu-id="979cd-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="979cd-114">Приложения используют интерфейс SSPI для поставщика безопасности [безопасного канала](secure-channel.md) (Schannel) для реализации безопасности WinInet.</span><span class="sxs-lookup"><span data-stu-id="979cd-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="979cd-115">Schannel — это реализация SSL в корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="979cd-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="979cd-116">Несколько функций SSPI возвращают метки времени, представляющие продолжительность различных объектов.</span><span class="sxs-lookup"><span data-stu-id="979cd-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="979cd-117">[*Пакеты безопасности*](../secgloss/s-gly.md) могут поддерживать время и задавать отметки времени различными способами, но использование местного времени упрощает работу приложений, использующих функции SSPI.</span><span class="sxs-lookup"><span data-stu-id="979cd-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 

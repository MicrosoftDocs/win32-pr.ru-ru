---
description: Команда СИОКГИФКОНФ, предоставляемая большинством реализаций UNIX, поддерживается в виде функций Всаиоктл и Вспиоктл с помощью команды SIO \_ Get \_ Interface \_ List. Эта команда возвращает список настроенных интерфейсов и их параметров.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Использование ioctl через UNIX в Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693162"
---
# <a name="using-unix-ioctls-in-winsock"></a><span data-ttu-id="bda1a-104">Использование ioctl через UNIX в Winsock</span><span class="sxs-lookup"><span data-stu-id="bda1a-104">Using UNIX Ioctls in Winsock</span></span>

<span data-ttu-id="bda1a-105">Команда **сиокгифконф** , предоставляемая большинством реализаций UNIX, поддерживается в виде функций [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) и [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) с помощью команды **SIO \_ Get \_ Interface \_ List**.</span><span class="sxs-lookup"><span data-stu-id="bda1a-105">The **SIOCGIFCONF** command provided by most UNIX implementations is supported in the form of [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) functions with the command **SIO\_GET\_INTERFACE\_LIST**.</span></span> <span data-ttu-id="bda1a-106">Эта команда возвращает список настроенных интерфейсов и их параметров.</span><span class="sxs-lookup"><span data-stu-id="bda1a-106">This command returns the list of configured interfaces and their parameters.</span></span>

> [!Note]  
> <span data-ttu-id="bda1a-107">Эта команда является обязательной для поставщиков служб TCP/IP, совместимых с Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="bda1a-107">Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.</span></span>

 

<span data-ttu-id="bda1a-108">Параметр *лпваутбуффер* указывает на буфер, в котором [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) и [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) хранят сведения об интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="bda1a-108">The parameter *lpvOutBuffer* points to the buffer in which [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) store the information about interfaces.</span></span> <span data-ttu-id="bda1a-109">Количество интерфейсов (число структур, возвращаемых в *лпваутбуффер*) можно определить на основе фактической длины выходного буфера, возвращаемого в *лпкббитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="bda1a-109">The number of interfaces (number of structures returned in *lpvOutBuffer*) can be determined based on the actual length of the output buffer returned in *lpcbBytesReturned*.</span></span>

 

 

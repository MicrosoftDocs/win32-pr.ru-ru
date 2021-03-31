---
title: Поставщики безопасности
description: Интерфейс поставщика поддержки безопасности (SSPI) обеспечивает взаимную проверку подлинности и предоставляется напрямую через интерфейсы API и службы SSPI, включенные на уровне SSPI, включая RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067354"
---
# <a name="security-providers"></a><span data-ttu-id="1778f-103">Поставщики безопасности</span><span class="sxs-lookup"><span data-stu-id="1778f-103">Security Providers</span></span>

<span data-ttu-id="1778f-104">Интерфейс поставщика поддержки безопасности (SSPI) обеспечивает взаимную проверку подлинности и предоставляется напрямую через интерфейсы API и службы SSPI, включенные на уровне SSPI, включая RPC.</span><span class="sxs-lookup"><span data-stu-id="1778f-104">The Security Support Provider Interface (SSPI) provides support for mutual authentication and is exposed directly through the SSPI APIs and services layered on SSPI, including RPC.</span></span>

<span data-ttu-id="1778f-105">Не все пакеты безопасности, доступные для SSPI, поддерживают взаимную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="1778f-105">Not all security packages available to SSPI support mutual authentication.</span></span> <span data-ttu-id="1778f-106">Чтобы получить взаимную проверку подлинности, приложение должно запросить взаимную проверку подлинности и пакет безопасности, который его поддерживает.</span><span class="sxs-lookup"><span data-stu-id="1778f-106">To obtain mutual authentication, the application must request mutual authentication and a security package that supports it.</span></span> <span data-ttu-id="1778f-107">Например, пример кода для [взаимной проверки подлинности в службе сокетов Windows с SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) использует пакет "Negotiate" в Secur32.dll, который входит в состав Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1778f-107">For example, the code example in [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) uses the "negotiate" package in Secur32.dll, which is included with Windows 2000.</span></span>

 

 





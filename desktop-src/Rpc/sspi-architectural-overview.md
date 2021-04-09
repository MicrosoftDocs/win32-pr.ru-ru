---
title: Обзор архитектуры SSPI
description: SSPI — это программный интерфейс.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070350"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="eb6ce-103">Обзор архитектуры SSPI</span><span class="sxs-lookup"><span data-stu-id="eb6ce-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="eb6ce-104">SSPI — это программный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-104">SSPI is a software interface.</span></span> <span data-ttu-id="eb6ce-105">Такие библиотеки распределенного программирования, как RPC, могут использовать ее для подключений, прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="eb6ce-106">Один или несколько программных модулей предоставляют действительные возможности проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="eb6ce-107">Каждый модуль, называемый поставщиком поддержки безопасности (SSP), реализуется как библиотека динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="eb6ce-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="eb6ce-108">Поставщик общих служб предоставляет один или несколько пакетов безопасности.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="eb6ce-109">Доступны разнообразные SSP и пакеты.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="eb6ce-110">Windows поставляется с пакетом безопасности NTLM и пакетом безопасности протокола Microsoft Kerberos.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="eb6ce-111">Кроме того, можно выбрать установку пакета безопасности SSL или любого другого поставщика, совместимого с SSPI.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="eb6ce-112">Использование SSPI гарантирует, что независимо от выбранного поставщика общих служб приложение будет обращаться к функциям проверки подлинности единообразно.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="eb6ce-113">Эта возможность обеспечивает более высокую независимость приложения от реализации сети, чем было доступно в прошлом.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="eb6ce-114">Распределенные приложения обмениваются данными через интерфейс RPC.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="eb6ce-115">Программное обеспечение RPC, в свою очередь, обращается к функциям проверки подлинности SSP через SSPI.</span><span class="sxs-lookup"><span data-stu-id="eb6ce-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="eb6ce-116">Дополнительные сведения см. в разделе [SSPI](/windows/desktop/SecAuthN/sspi).</span><span class="sxs-lookup"><span data-stu-id="eb6ce-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 
---
description: Объясняет, как создать пользовательский пакет безопасности.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Создание пользовательских пакетов безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910635"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="279f5-103">Создание пользовательских пакетов безопасности</span><span class="sxs-lookup"><span data-stu-id="279f5-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="279f5-104">Пакеты безопасности SSP</span><span class="sxs-lookup"><span data-stu-id="279f5-104">SSP Security Packages</span></span>

<span data-ttu-id="279f5-105">Если пакет безопасности пользовательского поставщика поддержки безопасности (SSP) будет использоваться исключительно для обеспечения безопасности клиента или сервера, он может реализовать [интерфейс поставщика поддержки безопасности](sspi.md)Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="279f5-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="279f5-106">Пример Сампссп, поставляемый с пакетом SDK для платформы, содержит пример реализации пакета безопасности SSP.</span><span class="sxs-lookup"><span data-stu-id="279f5-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="279f5-107">Пакеты безопасности SSP и AP</span><span class="sxs-lookup"><span data-stu-id="279f5-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="279f5-108">Собственные [](/windows/desktop/SecGloss/s-gly) / [*пакеты проверки подлинности*](/windows/desktop/SecGloss/a-gly) поставщика поддержки безопасности (SSP или ТД) содержат пакеты безопасности, которые работают как пакеты проверки подлинности (ТД) и поставщики поддержки безопасности (SSP).</span><span class="sxs-lookup"><span data-stu-id="279f5-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="279f5-109">Эти пакеты реализуют отдельные интерфейсы API для поддержки каждой роли.</span><span class="sxs-lookup"><span data-stu-id="279f5-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="279f5-110">Поскольку он функционирует как ТД, Пользовательский [*пакет безопасности*](/windows/desktop/SecGloss/s-gly) SSP или AP должен предоставить реализации для всех [функций, реализованных пакетами проверки подлинности](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="279f5-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="279f5-111">Чтобы обеспечить интегрированную поддержку безопасности, пользовательский пакет безопасности SSP или AP должен предоставить реализации [функций, реализуемых SSP или ТД](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="279f5-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="279f5-112">[Функции LSA, вызываемые SSP или ТД](authentication-functions.md) , описывают функции поддержки, доступные разработчикам SSP и AP, которые хотят взаимодействовать с LSA.</span><span class="sxs-lookup"><span data-stu-id="279f5-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="279f5-113">Пакеты безопасности SSP и AP, которые можно выполнять как в качестве ТД, так и в SSP, могут выполняться как часть операционной системы и как часть пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="279f5-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="279f5-114">Эти два режима выполнения известны как режим LSA и пользовательский режим соответственно.</span><span class="sxs-lookup"><span data-stu-id="279f5-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="279f5-115">Дополнительные сведения о пользовательских пакетах безопасности в режиме LSA см. в разделе [Инициализация режима LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="279f5-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="279f5-116">Дополнительные сведения о пользовательском режиме см. в разделе [Инициализация пользовательского режима](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="279f5-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="279f5-117">Если пользовательский пакет безопасности SSP или AP предлагает службы для клиентских и серверных приложений, он должен предоставить реализации для функций, описанных в разделе [функции, реализованные с помощью SSP или ТД пользовательского режима](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="279f5-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="279f5-118">[Функции LSA, вызываемые SSP или ТД пользовательского режима](authentication-functions.md) , описывают функции поддержки, доступные для SSP или AP, исполняемые в процессе клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="279f5-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="279f5-119">Сведения о регистрации библиотеки DLL поставщика общих служб и AP см. в разделе [Регистрация DLL-библиотек SSP и AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="279f5-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="279f5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="279f5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="279f5-121">Ограничения, касающихся регистрации и установки пакета безопасности</span><span class="sxs-lookup"><span data-stu-id="279f5-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 

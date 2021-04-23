---
description: Описание различий между SSP и ТД и SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP, ТД и SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999145"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="f5ffd-103">SSP, ТД и SSP</span><span class="sxs-lookup"><span data-stu-id="f5ffd-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="f5ffd-104">[*Пакеты безопасности*](../secgloss/s-gly.md) развертываются в одном из следующих типов библиотек динамической компоновки (DLL):</span><span class="sxs-lookup"><span data-stu-id="f5ffd-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="f5ffd-105">SSP или ТД</span><span class="sxs-lookup"><span data-stu-id="f5ffd-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="f5ffd-106">Поставщиков</span><span class="sxs-lookup"><span data-stu-id="f5ffd-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="f5ffd-107">Независимо от того, входит ли пакет безопасности в состав поставщика поддержки безопасности или [*пакета проверки подлинности*](../secgloss/a-gly.md) (SSP/AP) или [*поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSP), он определяется типами предоставляемых служб безопасности и степенью интеграции с [*локальным центром безопасности*](../secgloss/l-gly.md) (LSA).</span><span class="sxs-lookup"><span data-stu-id="f5ffd-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="f5ffd-108">Эти различия также определяют интерфейс API, реализованный в пользовательском пакете безопасности.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="f5ffd-109">SSP или ТД</span><span class="sxs-lookup"><span data-stu-id="f5ffd-109">SSP/APs</span></span>

<span data-ttu-id="f5ffd-110">SSP или AP — это библиотека DLL, которая содержит один или несколько [*пакетов безопасности*](../secgloss/s-gly.md) и может функционировать как поставщик общих служб для клиентских и серверных приложений и как [пакет проверки подлинности](authentication-packages.md) для приложений для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="f5ffd-111">Для функционирования обеих этих ролей SSP и ТД загружаются в пространство процесса LSA при запуске системы и могут быть загружены в процессы приложений клиента/сервера.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="f5ffd-112">В пользовательских пакетах безопасности SSP и AP должны быть реализованы [функции, реализуемые SSP или ТД пользовательского режима](authentication-functions.md), а также [функции, реализованные SSP или ТД](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f5ffd-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="f5ffd-113">Эти реализации функций могут использовать функции поддержки LSA для предоставления расширенных функций безопасности, таких как создание маркеров, поддержка [*дополнительных учетных данных*](../secgloss/s-gly.md) и сквозная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="f5ffd-114">Если пользовательский пакет безопасности SSP или AP предоставляет полный набор функций обеспечения [*целостности*](../secgloss/i-gly.md) и конфиденциальности сообщений, он также реализует [функции, реализованные SSP и ТД пользовательского режима](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f5ffd-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="f5ffd-115">Поставщиков</span><span class="sxs-lookup"><span data-stu-id="f5ffd-115">SSPs</span></span>

<span data-ttu-id="f5ffd-116">SSP — это библиотека DLL, которая содержит один или несколько пакетов безопасности, обеспечивающих проверку подлинности подключений, целостности сообщений и служб шифрования сообщений для клиентских и серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="f5ffd-117">SSP реализуют функции [интерфейса поставщика поддержки безопасности](sspi.md) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="f5ffd-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="f5ffd-118">Приложения могут получать доступ к пакетам безопасности в поставщике общих служб, вызывая функции SSPI напрямую.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="f5ffd-119">SSP загружаются в процессы клиента и сервера; они не интегрированы с LSA.</span><span class="sxs-lookup"><span data-stu-id="f5ffd-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 

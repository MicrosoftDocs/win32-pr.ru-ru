---
description: Использование интерфейсов API родительского контроля
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Использование интерфейсов API родительского контроля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719501"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="2e990-103">Использование интерфейсов API родительского контроля</span><span class="sxs-lookup"><span data-stu-id="2e990-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="2e990-104">Выбор API</span><span class="sxs-lookup"><span data-stu-id="2e990-104">API Selection</span></span>

<span data-ttu-id="2e990-105">Как отмечалось в разделе "Обзор", в разработке предполагается использование до трех интерфейсов API:</span><span class="sxs-lookup"><span data-stu-id="2e990-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="2e990-106">Основные параметры доступ: API-интерфейс с минимальным соответствием для родительского контроля (API соответствия), определенный в Впкапи. h, для простого доступа к подмножеству ключей родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="2e990-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="2e990-107">Полная настройка доступа для записи и чтения. Использование небольшого подмножества API COM WMI для полного доступа требуется только в том случае, если поставщику программного обеспечения необходимо изменить параметры.</span><span class="sxs-lookup"><span data-stu-id="2e990-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="2e990-108">Основной причиной использования API является добавление ссылки на расширяемость пользовательского интерфейса, замену фильтра веб-содержимого или дополнений к спискам исключений для приложения HTTP или фильтрации URL-адресов на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="2e990-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="2e990-109">Поскольку использование пространства имен "родительский контроль WMI" предоставляет необработанный доступ к базовому хранилищу параметров, независимые поставщики программного обеспечения должны соблюдать осторожность при интерпретации состояния отдельных параметров, которые могут фактически иметь зависимости от других параметров.</span><span class="sxs-lookup"><span data-stu-id="2e990-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="2e990-110">Поэтому рекомендуется использовать API соответствия для чтения состояния для всех значений, предоставляемых этим API.</span><span class="sxs-lookup"><span data-stu-id="2e990-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="2e990-111">Ведение журнала. системный API трассировки и отчетов Windows Vista (также называемый ETW) для публикации событий действий в журналах родительского контроля в сочетании с дескрипторами событий и перечислениями массивов, определенными в Впцевент. h.</span><span class="sxs-lookup"><span data-stu-id="2e990-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="2e990-112">Все API-интерфейсы вызываемы как обычные пользователи.</span><span class="sxs-lookup"><span data-stu-id="2e990-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="2e990-113">Для ведения журнала любой пользователь может вести журнал событий.</span><span class="sxs-lookup"><span data-stu-id="2e990-113">For logging, any user may source log events.</span></span> <span data-ttu-id="2e990-114">Вызов для получения или изменения параметров другого пользователя завершится ошибкой, если вызывающий объект не имеет прав администратора.</span><span class="sxs-lookup"><span data-stu-id="2e990-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="2e990-115">Иными словами, обычный пользователь может получить доступ только к его собственным параметрам и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e990-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="2e990-116">Параметры и использование API для ведения журнала обсуждаются далее в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2e990-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="2e990-117">Использование API параметров родительского контроля</span><span class="sxs-lookup"><span data-stu-id="2e990-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="2e990-118">Использование API ведения журнала для родительского контроля</span><span class="sxs-lookup"><span data-stu-id="2e990-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="2e990-119">Среда разработки</span><span class="sxs-lookup"><span data-stu-id="2e990-119">Development Environment</span></span>

<span data-ttu-id="2e990-120">Для разработки для родительских элементов управления требуется доступ к трем файлам заголовков: WPC. h, Впкапи. h и Впцевент. h.</span><span class="sxs-lookup"><span data-stu-id="2e990-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="2e990-121">WPC. h — это сборщик, который включает в себя параметры общедоступного API соответствия и заголовков событий, поэтому в коде приложения достаточно включить WPC. h.</span><span class="sxs-lookup"><span data-stu-id="2e990-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="2e990-122">Разрешения на чтение и запись для API WMI указываются в файле Впкспров. mof.</span><span class="sxs-lookup"><span data-stu-id="2e990-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="2e990-123">Этот файл устанавливается в подкаталог WBEM в каталоге Windows System32.</span><span class="sxs-lookup"><span data-stu-id="2e990-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="2e990-124">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) содержит образец кода, который позволяет получить пример кода, приведенный здесь, и предоставляет простые средства, управляемые командной строкой для изучения API или интеграции.</span><span class="sxs-lookup"><span data-stu-id="2e990-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 




---
description: В этом разделе описывается, что необходимо сделать для начала создания программ, использующих API датчика.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Общие требования для разработки приложений (API-интерфейс датчика)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347645"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="d905d-103">Общие требования для разработки приложений (API-интерфейс датчика)</span><span class="sxs-lookup"><span data-stu-id="d905d-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="d905d-104">В этом разделе описывается, что необходимо сделать для начала создания программ, использующих API датчика.</span><span class="sxs-lookup"><span data-stu-id="d905d-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="d905d-105">Чтобы создать приложение API датчика, необходимо установить Windows 7 и пакет средств разработки программного обеспечения (SDK) Windows 7 на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d905d-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="d905d-106">В следующей таблице описаны конкретные файлы, которые потребуются.</span><span class="sxs-lookup"><span data-stu-id="d905d-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="d905d-107">Имя файла</span><span class="sxs-lookup"><span data-stu-id="d905d-107">File name</span></span>               | <span data-ttu-id="d905d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d905d-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d905d-109">Сенсорсапи. h</span><span class="sxs-lookup"><span data-stu-id="d905d-109">Sensorsapi.h</span></span>            | <span data-ttu-id="d905d-110">Основной файл заголовка для API датчика.</span><span class="sxs-lookup"><span data-stu-id="d905d-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="d905d-111">Этот файл заголовка содержит определения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d905d-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="d905d-112">Sensors. h</span><span class="sxs-lookup"><span data-stu-id="d905d-112">Sensors.h</span></span>               | <span data-ttu-id="d905d-113">Файл заголовка, содержащий определения констант, определенных платформой.</span><span class="sxs-lookup"><span data-stu-id="d905d-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="d905d-114">Инитгуид. h</span><span class="sxs-lookup"><span data-stu-id="d905d-114">Initguid.h</span></span>              | <span data-ttu-id="d905d-115">Файл заголовка, содержащий определения для управления инициализацией **GUID** .</span><span class="sxs-lookup"><span data-stu-id="d905d-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="d905d-116">Функтиондисковерикэйс. h</span><span class="sxs-lookup"><span data-stu-id="d905d-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="d905d-117">Файл заголовка, который определяет ключи свойств идентификатора устройства, необходимые при подключении к логическим датчикам.</span><span class="sxs-lookup"><span data-stu-id="d905d-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="d905d-118">Сенсорсапи. lib</span><span class="sxs-lookup"><span data-stu-id="d905d-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="d905d-119">Статическая библиотека, содержащая определения **GUID** для API датчика.</span><span class="sxs-lookup"><span data-stu-id="d905d-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="d905d-120">Портабледевицегуидс. lib</span><span class="sxs-lookup"><span data-stu-id="d905d-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="d905d-121">Статическая библиотека, содержащая определения **GUID** для объектов переносимых устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="d905d-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="d905d-122">Программа может потребовать дополнительные файлы.</span><span class="sxs-lookup"><span data-stu-id="d905d-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="d905d-123">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="d905d-123">Supported Operating Systems</span></span>

<span data-ttu-id="d905d-124">Приложения API датчика будут работать во всех выпусках Windows 7, за исключением выпуска Windows 7 Starter Edition.</span><span class="sxs-lookup"><span data-stu-id="d905d-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="d905d-125">Интерфейсы переносных устройств Windows</span><span class="sxs-lookup"><span data-stu-id="d905d-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="d905d-126">API датчика использует определенные объекты переносных устройств Windows (WPD) для инкапсуляции ключей и значений свойств.</span><span class="sxs-lookup"><span data-stu-id="d905d-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="d905d-127">В следующей таблице описаны интерфейсы для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="d905d-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="d905d-128">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d905d-128">Interface</span></span>                                                                       | <span data-ttu-id="d905d-129">Описание</span><span class="sxs-lookup"><span data-stu-id="d905d-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d905d-130">[ипортабледевицевалуес](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d905d-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="d905d-131">Этот интерфейс предоставляет удобный способ создания контейнера свойств для пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="d905d-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="d905d-132">Имена представляются **PROPERTYKEY** s, а значения представлены **пропвариант** s.</span><span class="sxs-lookup"><span data-stu-id="d905d-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="d905d-133">API использует этот интерфейс для установки и извлечения одиночных значений и наборов значений.</span><span class="sxs-lookup"><span data-stu-id="d905d-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="d905d-134">Этот интерфейс можно получить из метода или, если требуется новый объект, вызвав **CoCreateInstance** с CLSID \_ портабледевицевалуес.</span><span class="sxs-lookup"><span data-stu-id="d905d-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="d905d-135">[ипортабледевицекэйколлектион](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d905d-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="d905d-136">Этот интерфейс содержит коллекцию **PROPERTYKEY** s.</span><span class="sxs-lookup"><span data-stu-id="d905d-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="d905d-137">Эти ключи представляют имена свойств, которые могут храниться в **ипортабледевицевалуес**.</span><span class="sxs-lookup"><span data-stu-id="d905d-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="d905d-138">API использует этот объект коллекции для задания и извлечения имен и наборов имен свойств, а также отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="d905d-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="d905d-139">Этот интерфейс можно получить из метода или, если требуется новый объект, вызвав **CoCreateInstance** с CLSID \_ портабледевицекэйколлектион.</span><span class="sxs-lookup"><span data-stu-id="d905d-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 


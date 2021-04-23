---
description: Устройство может создавать много событий, и каждое событие имеет возможность обработки одним из нескольких различных обработчиков.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Регистрация обработчика событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985421"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="7e013-103">Регистрация обработчика событий</span><span class="sxs-lookup"><span data-stu-id="7e013-103">How to Register an Event Handler</span></span>

<span data-ttu-id="7e013-104">Устройство может создавать много событий, и каждое событие имеет возможность обработки одним из нескольких различных обработчиков.</span><span class="sxs-lookup"><span data-stu-id="7e013-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="7e013-105">В Windows XP определены следующие события:</span><span class="sxs-lookup"><span data-stu-id="7e013-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="7e013-106">девицеарривал</span><span class="sxs-lookup"><span data-stu-id="7e013-106">DeviceArrival</span></span>
-   <span data-ttu-id="7e013-107">девицеремовал</span><span class="sxs-lookup"><span data-stu-id="7e013-107">DeviceRemoval</span></span>
-   <span data-ttu-id="7e013-108">медиаарривал</span><span class="sxs-lookup"><span data-stu-id="7e013-108">MediaArrival</span></span>
-   <span data-ttu-id="7e013-109">медиаремовал</span><span class="sxs-lookup"><span data-stu-id="7e013-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="7e013-110">Инструкции</span><span class="sxs-lookup"><span data-stu-id="7e013-110">Instructions</span></span>


<span data-ttu-id="7e013-111">Обработчики событий определяются в ключе **евенсандлерс** .</span><span class="sxs-lookup"><span data-stu-id="7e013-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="7e013-112">Значения ключа обработчика событий — это имена всех обработчиков, которые пользователь должен выбрать при обнаружении события.</span><span class="sxs-lookup"><span data-stu-id="7e013-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="7e013-113">С этими записями не связано значение данных.</span><span class="sxs-lookup"><span data-stu-id="7e013-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="7e013-114">Ниже приведен пример определения пользовательского обработчика событий с именем **миневремовалевенсандлер**, который предоставляет пользователю возможности обработчика:</span><span class="sxs-lookup"><span data-stu-id="7e013-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="7e013-115">Обработчик, используемый при обнаружении события на устройстве, созданном компанией Contoso, Inc.</span><span class="sxs-lookup"><span data-stu-id="7e013-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="7e013-116">Обработчик, используемый при обнаружении события на устройстве, которое компания называется Fabrikam, Inc.</span><span class="sxs-lookup"><span data-stu-id="7e013-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="7e013-117">Обработчик, используемый во всех остальных случаях.</span><span class="sxs-lookup"><span data-stu-id="7e013-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="7e013-118">После определения обработчика событий он должен быть зарегистрирован в обработчике устройства для одного из возможных событий: Девицеарривал, Девицеремовал, Медиаарривал или Медиаремовал.</span><span class="sxs-lookup"><span data-stu-id="7e013-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="7e013-119">Миневремовалевенсандлер, определенный ранее, используется для Девицеремовал в пользовательском обработчике устройства с именем Мидевицехандлер и определяется для этой цели в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7e013-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="7e013-120">Опять же, значение реестра не содержит компонентов данных.</span><span class="sxs-lookup"><span data-stu-id="7e013-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="7e013-121">Windows XP определяет следующий набор Евенсандлерс.</span><span class="sxs-lookup"><span data-stu-id="7e013-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="7e013-122">Ключ Евенсандлерс</span><span class="sxs-lookup"><span data-stu-id="7e013-122">EventHandlers key</span></span>        | <span data-ttu-id="7e013-123">Носитель или тип файла</span><span class="sxs-lookup"><span data-stu-id="7e013-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="7e013-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="7e013-125">Чистый компакт-диск — R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="7e013-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="7e013-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="7e013-127">Файлы изображений</span><span class="sxs-lookup"><span data-stu-id="7e013-127">Picture files</span></span>                                  |
| <span data-ttu-id="7e013-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="7e013-129">Музыкальные файлы</span><span class="sxs-lookup"><span data-stu-id="7e013-129">Music files</span></span>                                    |
| <span data-ttu-id="7e013-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="7e013-131">Видеофайлы</span><span class="sxs-lookup"><span data-stu-id="7e013-131">Video files</span></span>                                    |
| <span data-ttu-id="7e013-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="7e013-133">Аудио компакт-диск (формат РЕДБУК с аудио-дорожкой)</span><span class="sxs-lookup"><span data-stu-id="7e013-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="7e013-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="7e013-135">Фильмы DVD</span><span class="sxs-lookup"><span data-stu-id="7e013-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="7e013-136">В дополнение к указанным выше параметрам Windows Vista предопределяется следующий набор Евенсандлерс.</span><span class="sxs-lookup"><span data-stu-id="7e013-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="7e013-137">Ключ Евенсандлерс</span><span class="sxs-lookup"><span data-stu-id="7e013-137">EventHandlers key</span></span>              | <span data-ttu-id="7e013-138">Носитель или тип файла</span><span class="sxs-lookup"><span data-stu-id="7e013-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="7e013-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="7e013-140">Фильмы Super Видеокд</span><span class="sxs-lookup"><span data-stu-id="7e013-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="7e013-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="7e013-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="7e013-142">Фильмы Видеокд</span><span class="sxs-lookup"><span data-stu-id="7e013-142">VideoCD movies</span></span>       |



 

 

 




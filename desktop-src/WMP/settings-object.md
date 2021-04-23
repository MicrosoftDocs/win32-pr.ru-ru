---
title: Объект Settings (пакет SDK для проигрывателя Windows Media)
description: Объект параметров предоставляет способ изменения различных параметров проигрывателя Windows Media с помощью следующих свойств и методов.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Проигрыватель Windows Media, объект параметров
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "103889975"
---
# <a name="settings-object"></a><span data-ttu-id="8730d-104">Объект параметров</span><span class="sxs-lookup"><span data-stu-id="8730d-104">Settings Object</span></span>

<span data-ttu-id="8730d-105">Объект **параметров** предоставляет способ изменения различных параметров проигрывателя Windows Media с помощью следующих свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="8730d-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="8730d-106">Объект **Settings** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8730d-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="8730d-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="8730d-107">Property</span></span>                                                  | <span data-ttu-id="8730d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8730d-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8730d-109">Автозапуска</span><span class="sxs-lookup"><span data-stu-id="8730d-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="8730d-110">Указывает или получает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.</span><span class="sxs-lookup"><span data-stu-id="8730d-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="8730d-111">между</span><span class="sxs-lookup"><span data-stu-id="8730d-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="8730d-112">Указывает или получает текущее стерео сальдо.</span><span class="sxs-lookup"><span data-stu-id="8730d-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="8730d-113">baseURL</span><span class="sxs-lookup"><span data-stu-id="8730d-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="8730d-114">Указывает или получает базовый URL-адрес, используемый для разрешения относительных путей с помощью команд сценария URL-адреса, внедренных в файлы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8730d-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="8730d-115">дефаултаудиолангуаже</span><span class="sxs-lookup"><span data-stu-id="8730d-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="8730d-116">Возвращает код локали (LCID) для языка по умолчанию, указанного в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8730d-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="8730d-117">дефаултфраме</span><span class="sxs-lookup"><span data-stu-id="8730d-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="8730d-118">Указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="8730d-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="8730d-119">енаблиррордиалогс</span><span class="sxs-lookup"><span data-stu-id="8730d-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="8730d-120">Указывает или получает значение, указывающее, отображаются ли диалоговые окна ошибок автоматически.</span><span class="sxs-lookup"><span data-stu-id="8730d-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="8730d-121">инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="8730d-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="8730d-122">Указывает или получает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="8730d-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="8730d-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="8730d-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="8730d-124">Определяет, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="8730d-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="8730d-125">медиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="8730d-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="8730d-126">Извлекает значение, указывающее права, предоставленные в настоящее время для доступа к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="8730d-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="8730d-127">отключен</span><span class="sxs-lookup"><span data-stu-id="8730d-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="8730d-128">Указывает или получает значение, указывающее, отключено ли звуковое сопровождение.</span><span class="sxs-lookup"><span data-stu-id="8730d-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="8730d-129">плайкаунт</span><span class="sxs-lookup"><span data-stu-id="8730d-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="8730d-130">Указывает или получает количество попыток воспроизведения элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8730d-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="8730d-131">курсе</span><span class="sxs-lookup"><span data-stu-id="8730d-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="8730d-132">Указывает или получает текущую скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8730d-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="8730d-133">тома</span><span class="sxs-lookup"><span data-stu-id="8730d-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="8730d-134">Указывает или получает текущий том.</span><span class="sxs-lookup"><span data-stu-id="8730d-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="8730d-135">Объект **Settings** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8730d-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="8730d-136">Метод</span><span class="sxs-lookup"><span data-stu-id="8730d-136">Method</span></span>                                                            | <span data-ttu-id="8730d-137">Описание</span><span class="sxs-lookup"><span data-stu-id="8730d-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="8730d-138">Режим</span><span class="sxs-lookup"><span data-stu-id="8730d-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="8730d-139">Определяет, активен ли режим "цикл" или "случайный".</span><span class="sxs-lookup"><span data-stu-id="8730d-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="8730d-140">рекуестмедиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="8730d-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="8730d-141">Запрашивает указанный уровень доступа к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="8730d-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="8730d-142">setMode</span><span class="sxs-lookup"><span data-stu-id="8730d-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="8730d-143">Устанавливает режим цикла или случайный режим на активный или неактивный.</span><span class="sxs-lookup"><span data-stu-id="8730d-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="8730d-144">Доступ к объекту **параметров** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8730d-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="8730d-145">Объект</span><span class="sxs-lookup"><span data-stu-id="8730d-145">Object</span></span>                      | <span data-ttu-id="8730d-146">Свойство</span><span class="sxs-lookup"><span data-stu-id="8730d-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="8730d-147">Игрок</span><span class="sxs-lookup"><span data-stu-id="8730d-147">Player</span></span>](player-object.md) | [<span data-ttu-id="8730d-148">параметры</span><span class="sxs-lookup"><span data-stu-id="8730d-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="8730d-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8730d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8730d-150">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="8730d-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





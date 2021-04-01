---
title: Объект Profile
description: Объект Profile
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Пакет SDK для Windows Media Format, объекты профилирования
- Расширенный системный формат (ASF), объекты профилирования
- ASF (Расширенный системный формат), объекты профилирования
- объекты, объекты профилирования
- профили, объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103890315"
---
# <a name="profile-object"></a><span data-ttu-id="25eee-108">Объект Profile</span><span class="sxs-lookup"><span data-stu-id="25eee-108">Profile Object</span></span>

<span data-ttu-id="25eee-109">Объект профиля управляет параметрами профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="25eee-110">Объекты профиля могут быть созданы для существующих данных профиля или могут быть созданы пустыми и готовы к получению новых данных.</span><span class="sxs-lookup"><span data-stu-id="25eee-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="25eee-111">Объект профиля также создается объектом модуля чтения (и синхронным объектом Reader) при загрузке файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="25eee-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="25eee-112">В этом случае объект заполняется сведениями профиля, хранящимися в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="25eee-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="25eee-113">Чтобы сохранить содержимое объекта профиля, необходимо вызвать метод [**ивмпрофилеманажер:: савепрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span><span class="sxs-lookup"><span data-stu-id="25eee-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="25eee-114">Профиль содержит несколько объектов, управляющих различными аспектами профиля (например, потоками).</span><span class="sxs-lookup"><span data-stu-id="25eee-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="25eee-115">Все эти объекты являются подчиненными для объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="25eee-116">Эти объекты не создаются с помощью функций создания, как и для основных объектов этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="25eee-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="25eee-117">Вместо этого интерфейсы объекта Profile содержат методы, создающие подчиненные объекты.</span><span class="sxs-lookup"><span data-stu-id="25eee-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="25eee-118">Чтобы создать объект профиля, вызовите один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="25eee-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="25eee-119">Метод</span><span class="sxs-lookup"><span data-stu-id="25eee-119">Method</span></span>                                                                                | <span data-ttu-id="25eee-120">Описание</span><span class="sxs-lookup"><span data-stu-id="25eee-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25eee-121">**Ивмпрофилеманажер:: Креатимптипрофиле**</span><span class="sxs-lookup"><span data-stu-id="25eee-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="25eee-122">Создает объект профиля без данных профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="25eee-123">**Ивмпрофилеманажер:: Лоадпрофилебидата**</span><span class="sxs-lookup"><span data-stu-id="25eee-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="25eee-124">Создает объект профиля, заполненный данными из профиля, сохраненного в виде строки.</span><span class="sxs-lookup"><span data-stu-id="25eee-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="25eee-125">Это единственный способ создать объект профиля с данными из настраиваемого профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="25eee-126">**Ивмпрофилеманажер:: Лоадпрофилебид**</span><span class="sxs-lookup"><span data-stu-id="25eee-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="25eee-127">Создает объект профиля, заполненный данными из системного профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="25eee-128">Определяет требуемый системный профиль с помощью идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="25eee-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="25eee-129">**Ивмпрофилеманажер:: Лоадсистемпрофиле**</span><span class="sxs-lookup"><span data-stu-id="25eee-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="25eee-130">Создает объект профиля, заполненный данными из системного профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="25eee-131">Использует индекс профиля для задания требуемого системного профиля.</span><span class="sxs-lookup"><span data-stu-id="25eee-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="25eee-132">Все методы в приведенной выше таблице устанавливают указатель на интерфейс **ивмпрофиле** .</span><span class="sxs-lookup"><span data-stu-id="25eee-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="25eee-133">Другие интерфейсы объекта Profile можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="25eee-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="25eee-134">Каждый объект профиля поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="25eee-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="25eee-135">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="25eee-135">Interface</span></span>                                  | <span data-ttu-id="25eee-136">Описание</span><span class="sxs-lookup"><span data-stu-id="25eee-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25eee-137">**ивмлангуажелист**</span><span class="sxs-lookup"><span data-stu-id="25eee-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="25eee-138">Управляет списком языков, поддерживаемых ASF-файлом.</span><span class="sxs-lookup"><span data-stu-id="25eee-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="25eee-139">**ивмпаккетсизе**</span><span class="sxs-lookup"><span data-stu-id="25eee-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="25eee-140">Определяет максимальный размер пакетов в файле.</span><span class="sxs-lookup"><span data-stu-id="25eee-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="25eee-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="25eee-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="25eee-142">Управляет минимальным размером пакетов в файле.</span><span class="sxs-lookup"><span data-stu-id="25eee-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="25eee-143">Наследует все методы **ивмпаккетсизе**.</span><span class="sxs-lookup"><span data-stu-id="25eee-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="25eee-144">**ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="25eee-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="25eee-145">Управляет основными параметрами и объектами, входящими в профиль.</span><span class="sxs-lookup"><span data-stu-id="25eee-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="25eee-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="25eee-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="25eee-147">Возвращает глобальный уникальный идентификатор (GUID), связанный с профилем.</span><span class="sxs-lookup"><span data-stu-id="25eee-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="25eee-148">Наследует все методы **ивмпрофиле**.</span><span class="sxs-lookup"><span data-stu-id="25eee-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="25eee-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="25eee-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="25eee-150">Управляет доступом к пропускной способности и сведениями о приоритетах потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="25eee-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="25eee-151">Наследует все методы **ивмпрофиле** и **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="25eee-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="25eee-152">См. также</span><span class="sxs-lookup"><span data-stu-id="25eee-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25eee-153">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="25eee-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="25eee-154">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="25eee-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="25eee-155">**Профили**</span><span class="sxs-lookup"><span data-stu-id="25eee-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 





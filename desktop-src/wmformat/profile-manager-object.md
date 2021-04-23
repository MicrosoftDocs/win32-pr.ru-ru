---
title: Объект диспетчера профилей
description: Объект диспетчера профилей
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Пакет SDK Windows Media Format, объекты диспетчера профилей
- Расширенный системный формат (ASF), объекты диспетчера профилей
- ASF (Расширенный системный формат), объекты диспетчера профилей
- объекты, объекты диспетчера профилей
- профили, объекты
- профили, объекты диспетчера профилей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105710253"
---
# <a name="profile-manager-object"></a><span data-ttu-id="7346c-109">Объект диспетчера профилей</span><span class="sxs-lookup"><span data-stu-id="7346c-109">Profile Manager Object</span></span>

<span data-ttu-id="7346c-110">Профиль — это набор параметров носителя, используемых для создания файла ASF.</span><span class="sxs-lookup"><span data-stu-id="7346c-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="7346c-111">Объект диспетчера профилей создает объекты профиля для редактирования.</span><span class="sxs-lookup"><span data-stu-id="7346c-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="7346c-112">Объекты профиля могут создаваться без каких бы то ни было данных или построены из существующих данных профиля.</span><span class="sxs-lookup"><span data-stu-id="7346c-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="7346c-113">Объект диспетчера профилей также предоставляет методы для перечисления поддерживаемых кодеков и запроса информации для этих кодеков.</span><span class="sxs-lookup"><span data-stu-id="7346c-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="7346c-114">Объект диспетчера профилей создается функцией [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , которая устанавливает указатель на интерфейс [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="7346c-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="7346c-115">Другие интерфейсы объекта диспетчера профилей можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="7346c-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="7346c-116">Объект диспетчера профилей поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="7346c-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="7346c-117">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="7346c-117">Interface</span></span>                                                      | <span data-ttu-id="7346c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7346c-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7346c-119">**ивмкодеЦинфо**</span><span class="sxs-lookup"><span data-stu-id="7346c-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="7346c-120">Извлекает сведения о поддерживаемых кодеках и их форматах.</span><span class="sxs-lookup"><span data-stu-id="7346c-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="7346c-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="7346c-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="7346c-122">Извлекает имена поддерживаемых кодеков и описания их форматов.</span><span class="sxs-lookup"><span data-stu-id="7346c-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="7346c-123">Наследует все методы **ивмкодеЦинфо**.</span><span class="sxs-lookup"><span data-stu-id="7346c-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="7346c-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="7346c-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="7346c-125">Извлекает свойства кодека и запросы для поддерживаемых функций.</span><span class="sxs-lookup"><span data-stu-id="7346c-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="7346c-126">Наследует все методы **ивмкодеЦинфо** и **IWMCodecInfo2**.</span><span class="sxs-lookup"><span data-stu-id="7346c-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="7346c-127">**ивмпрофилеманажер**</span><span class="sxs-lookup"><span data-stu-id="7346c-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="7346c-128">Создает новые профили, загружает существующие профили и сохраняет пользовательские профили.</span><span class="sxs-lookup"><span data-stu-id="7346c-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="7346c-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="7346c-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="7346c-130">Управляет версией системных профилей, перечисленных диспетчером профилей.</span><span class="sxs-lookup"><span data-stu-id="7346c-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="7346c-131">Наследует все методы **ивмпрофилеманажер**.</span><span class="sxs-lookup"><span data-stu-id="7346c-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="7346c-132">**ивмпрофилеманажерлангуаже**</span><span class="sxs-lookup"><span data-stu-id="7346c-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="7346c-133">Управляет языком системных профилей, проанализированных диспетчером профилей.</span><span class="sxs-lookup"><span data-stu-id="7346c-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="7346c-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7346c-134">Remarks</span></span>

<span data-ttu-id="7346c-135">При создании объекта диспетчера профилей он анализирует все системные профили, что может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="7346c-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="7346c-136">Создание и выпуск диспетчера профилей каждый раз, когда потребуется его использовать, может негативно сказаться на производительности.</span><span class="sxs-lookup"><span data-stu-id="7346c-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="7346c-137">Вы должны создать диспетчер профилей один раз в своем приложении и освободить его только тогда, когда вам больше не понадобится его использовать.</span><span class="sxs-lookup"><span data-stu-id="7346c-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7346c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7346c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7346c-139">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="7346c-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="7346c-140">**Объект Profile**</span><span class="sxs-lookup"><span data-stu-id="7346c-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="7346c-141">**Профили**</span><span class="sxs-lookup"><span data-stu-id="7346c-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 





---
title: Интерфейс IWMProfile
description: Интерфейс Ивмпрофиле является основным интерфейсом для объекта профиля.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Формат Windows Media в интерфейсе Ивмпрофиле
- Ивмпрофиле интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "105661791"
---
# <a name="iwmprofile-interface"></a><span data-ttu-id="d3fd4-105">Интерфейс IWMProfile</span><span class="sxs-lookup"><span data-stu-id="d3fd4-105">IWMProfile interface</span></span>

<span data-ttu-id="d3fd4-106">Интерфейс **ивмпрофиле** является основным интерфейсом для объекта [*профиля*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="d3fd4-106">The **IWMProfile** interface is the primary interface for a [*profile*](wmformat-glossary.md) object.</span></span> <span data-ttu-id="d3fd4-107">Объект профиля используется для настройки пользовательских профилей.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-107">A profile object is used to configure custom profiles.</span></span> <span data-ttu-id="d3fd4-108">**Ивмпрофиле** можно использовать для создания, удаления или изменения объектов конфигурации потока и взаимоисключающих объектов.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-108">You can use **IWMProfile** to create, delete, or modify stream configuration objects and mutual exclusion objects.</span></span> <span data-ttu-id="d3fd4-109">Можно также задать и получить общие сведения о профиле.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-109">You can also set and retrieve general information about the profile.</span></span> <span data-ttu-id="d3fd4-110">Чтобы получить доступ ко всем функциям объекта Profile, следует использовать [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), который наследует от **ивмпрофиле** и [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span><span class="sxs-lookup"><span data-stu-id="d3fd4-110">To access all the features of the profile object, you should use [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), which inherits from **IWMProfile** and [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span></span>

<span data-ttu-id="d3fd4-111">**Ивмпрофиле** также доступен через объект Reader, где его можно использовать для получения сведений о потоках файла, загружаемого в средство чтения.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-111">**IWMProfile** is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader.</span></span> <span data-ttu-id="d3fd4-112">При доступе к **ивмпрофиле** из средства чтения можно вносить изменения в профиль, но ни один из изменений не может быть сохранен в файле.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-112">When accessing **IWMProfile** from the reader, you can make changes to the profile, but none of the changes can be saved to the file.</span></span> <span data-ttu-id="d3fd4-113">Часто бывает удобно использовать профиль существующего файла в качестве основы нового профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-113">It is often handy to use the profile of an existing file as the foundation of a new profile.</span></span> <span data-ttu-id="d3fd4-114">Синхронный модуль чтения поддерживает **ивмпрофиле** таким же образом, как и читатель.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-114">The synchronous reader supports **IWMProfile** in the same way as the reader.</span></span>

<span data-ttu-id="d3fd4-115">Данные профиля, полученные с помощью средства чтения или синхронного модуля чтения, не поступают из пркс-файла.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-115">The profile information obtained through the reader or synchronous reader does not come from a .prx file.</span></span> <span data-ttu-id="d3fd4-116">Средство чтения использует сведения в файле ASF для сборки конфигураций потоков.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-116">The reader uses the information in the ASF file to assemble the stream configurations.</span></span> <span data-ttu-id="d3fd4-117">Поэтому некоторые сведения о профиле, такие как имя и описание, недоступны через средство чтения.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-117">Thus certain profile information, like the name and description, are not available through the reader.</span></span>

<span data-ttu-id="d3fd4-118">Существует несколько способов получить указатель на интерфейс **ивмпрофиле** .</span><span class="sxs-lookup"><span data-stu-id="d3fd4-118">There are several ways to obtain a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="d3fd4-119">Диспетчер профилей имеет методы для создания нового профиля и доступа к существующим профилям.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-119">The profile manager has methods to create a new profile and to access existing profiles.</span></span> <span data-ttu-id="d3fd4-120">Все эти методы задают указатель **ивмпрофиле** .</span><span class="sxs-lookup"><span data-stu-id="d3fd4-120">All of these methods set an **IWMProfile** pointer.</span></span> <span data-ttu-id="d3fd4-121">При чтении файла указатель на **ивмпрофиле** можно получить, вызвав метод **QueryInterface** любого интерфейса чтения.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-121">When reading a file, a pointer to **IWMProfile** can be obtained by calling the **QueryInterface** method of any reader interface.</span></span> <span data-ttu-id="d3fd4-122">Аналогичным образом, любой интерфейс синхронного объекта Reader может получить указатель с вызовом **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span><span class="sxs-lookup"><span data-stu-id="d3fd4-122">Likewise, any interface of the synchronous reader object can obtain a pointer with a call to **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span></span>

## <a name="members"></a><span data-ttu-id="d3fd4-123">Элементы</span><span class="sxs-lookup"><span data-stu-id="d3fd4-123">Members</span></span>

<span data-ttu-id="d3fd4-124">Интерфейс **ивмпрофиле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d3fd4-124">The **IWMProfile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d3fd4-125">**Ивмпрофиле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d3fd4-125">**IWMProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="d3fd4-126">Методы</span><span class="sxs-lookup"><span data-stu-id="d3fd4-126">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3fd4-127">Методы</span><span class="sxs-lookup"><span data-stu-id="d3fd4-127">Methods</span></span>

<span data-ttu-id="d3fd4-128">Интерфейс **ивмпрофиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-128">The **IWMProfile** interface has these methods.</span></span>



| <span data-ttu-id="d3fd4-129">Метод</span><span class="sxs-lookup"><span data-stu-id="d3fd4-129">Method</span></span>                                                                  | <span data-ttu-id="d3fd4-130">Описание</span><span class="sxs-lookup"><span data-stu-id="d3fd4-130">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3fd4-131">**аддмутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-131">**AddMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | <span data-ttu-id="d3fd4-132">Добавляет объект взаимного исключения в профиль.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-132">Adds a mutual exclusion object to the profile.</span></span><br/>                                   |
| [<span data-ttu-id="d3fd4-133">**аддстреам**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-133">**AddStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | <span data-ttu-id="d3fd4-134">Добавляет поток в профиль.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-134">Adds a stream to the profile.</span></span><br/>                                                    |
| [<span data-ttu-id="d3fd4-135">**креатеневмутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-135">**CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="d3fd4-136">Создает объект взаимного исключения для профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-136">Creates a mutual exclusion object for the profile.</span></span><br/>                               |
| [<span data-ttu-id="d3fd4-137">**креатеневстреам**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-137">**CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | <span data-ttu-id="d3fd4-138">Создает объект конфигурации потока для профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-138">Creates a stream configuration object for the profile.</span></span><br/>                           |
| [<span data-ttu-id="d3fd4-139">**GetDescription**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-139">**GetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | <span data-ttu-id="d3fd4-140">Извлекает описание профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-140">Retrieves the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="d3fd4-141">**жетмутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-141">**GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="d3fd4-142">Извлекает объект взаимного исключения из профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-142">Retrieves a mutual exclusion object from the profile.</span></span><br/>                            |
| [<span data-ttu-id="d3fd4-143">**жетмутуалексклусионкаунт**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-143">**GetMutualExclusionCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | <span data-ttu-id="d3fd4-144">Возвращает количество объектов взаимного исключения в профиле.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-144">Retrieves the number of mutual exclusion objects in the profile.</span></span><br/>                 |
| [<span data-ttu-id="d3fd4-145">**GetName**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-145">**GetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | <span data-ttu-id="d3fd4-146">Возвращает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-146">Retrieves the name of the profile.</span></span><br/>                                               |
| [<span data-ttu-id="d3fd4-147">**GetStream**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-147">**GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | <span data-ttu-id="d3fd4-148">Извлекает из профиля поток, используя номер индекса.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-148">Retrieves a stream, using an index number, from the profile.</span></span><br/>                     |
| [<span data-ttu-id="d3fd4-149">**жетстреамбинумбер**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-149">**GetStreamByNumber**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | <span data-ttu-id="d3fd4-150">Извлекает поток, используя номер потока из профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-150">Retrieves a stream, using the number of the stream, from the profile.</span></span><br/>            |
| [<span data-ttu-id="d3fd4-151">**жетстреамкаунт**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-151">**GetStreamCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | <span data-ttu-id="d3fd4-152">Возвращает количество потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-152">Retrieves the number of streams in the profile.</span></span><br/>                                  |
| [<span data-ttu-id="d3fd4-153">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-153">**GetVersion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | <span data-ttu-id="d3fd4-154">Возвращает номер версии служб Microsoft Windows Media в профиле.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-154">Retrieves the version number of Microsoft Windows Media Services in the profile.</span></span><br/> |
| [<span data-ttu-id="d3fd4-155">**реконфигстреам**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-155">**ReconfigStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | <span data-ttu-id="d3fd4-156">Позволяет включить в профиль изменения, внесенные в конфигурацию потока.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-156">Enables changes made to a stream configuration to be included in the profile.</span></span><br/>    |
| [<span data-ttu-id="d3fd4-157">**ремовемутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-157">**RemoveMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | <span data-ttu-id="d3fd4-158">Удаляет объект взаимного исключения из профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-158">Removes a mutual exclusion object from the profile.</span></span><br/>                              |
| [<span data-ttu-id="d3fd4-159">**ремовестреам**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-159">**RemoveStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | <span data-ttu-id="d3fd4-160">Удаляет поток из профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-160">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="d3fd4-161">**ремовестреамбинумбер**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-161">**RemoveStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | <span data-ttu-id="d3fd4-162">Удаляет поток из профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-162">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="d3fd4-163">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-163">**SetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | <span data-ttu-id="d3fd4-164">Указывает описание профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-164">Specifies the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="d3fd4-165">**SetName**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-165">**SetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | <span data-ttu-id="d3fd4-166">Задает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-166">Specifies the name of the profile.</span></span><br/>                                               |



 

<span data-ttu-id="d3fd4-167">Сведения о том, какие интерфейсы можно получить с помощью метода QueryInterface этого интерфейса, см. в разделе, посвященном объекту, в котором реализован этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d3fd4-167">For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3fd4-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3fd4-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3fd4-169">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-169">**Interfaces**</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="d3fd4-170">**Интерфейс Ивмпрофилеманажер**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-170">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="d3fd4-171">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-171">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="d3fd4-172">**Объект модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-172">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="d3fd4-173">**Объект модуля синхронного чтения**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-173">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="d3fd4-174">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="d3fd4-174">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 


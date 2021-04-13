---
title: Загрузка системного профиля
description: Загрузка системного профиля
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- профили, система
- системные профили, Загрузка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412518"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="d8dcb-105">Загрузка системного профиля</span><span class="sxs-lookup"><span data-stu-id="d8dcb-105">To Load a System Profile</span></span>

<span data-ttu-id="d8dcb-106">Чтобы внести изменения в системный профиль, необходимо загрузить его в объект профиля.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="d8dcb-107">Диспетчер профилей предоставляет два варианта загрузки системных профилей: по идентификатору и по индексу.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="d8dcb-108">Идентификатор системного профиля — это значение GUID, назначенное системному профилю при его создании.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="d8dcb-109">Список констант GUID, связанных с системными профилями версии 8, см. в разделе [системные профили](system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="d8dcb-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="d8dcb-110">Константы GUID для предыдущих версий можно найти в файле заголовка Вмсиспрф. h.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="d8dcb-111">Дополнительные сведения об этом и других файлах заголовков, входящих в состав пакета SDK Windows Media Format, см. в разделе [файлы библиотек и параметры компилятора](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d8dcb-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="d8dcb-112">В следующем примере кода показано, как загрузить системный профиль с помощью идентификатора системного профиля.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="d8dcb-113">Чтобы этот код работал, необходимо включить Вмсиспрф. h и stdio. h.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="d8dcb-114">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="d8dcb-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="d8dcb-115">Если вы не уверены, какой профиль вы хотите использовать, можно выполнить итерацию по всем системным профилям определенной версии с помощью методов [**жетсистемпрофилекаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) и [**лоадсистемпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) интерфейса [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="d8dcb-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="d8dcb-116">В каждый момент времени эти методы работают только с одной версией системных профилей.</span><span class="sxs-lookup"><span data-stu-id="d8dcb-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="d8dcb-117">Дополнительные сведения об изменении версии системного профиля см. в разделе [изменение версий системного профиля](to-change-system-profile-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d8dcb-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8dcb-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d8dcb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8dcb-119">**Использование системных профилей**</span><span class="sxs-lookup"><span data-stu-id="d8dcb-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 





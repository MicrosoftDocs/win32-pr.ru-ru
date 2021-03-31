---
title: Создание профилей
description: Создание профилей
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK, профили
- профили, создание
- профили, интерфейс Ивмпрофилеманажер
- Ивмпрофилеманажер, создание профилей
- профили, функция Вмкреатепрофилеманажер
- вмкреатепрофилеманажер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069539"
---
# <a name="creating-profiles"></a><span data-ttu-id="54bf7-109">Создание профилей</span><span class="sxs-lookup"><span data-stu-id="54bf7-109">Creating Profiles</span></span>

<span data-ttu-id="54bf7-110">Во многих случаях потребуется создать пустой профиль для настройки.</span><span class="sxs-lookup"><span data-stu-id="54bf7-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="54bf7-111">В других случаях проще изменить существующий профиль, например системный профиль.</span><span class="sxs-lookup"><span data-stu-id="54bf7-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="54bf7-112">Дополнительные сведения об использовании системных профилей см. [в разделе Использование системных профилей](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="54bf7-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="54bf7-113">Создание пустого профиля, готового для настройки, требует наличия объекта диспетчера профилей.</span><span class="sxs-lookup"><span data-stu-id="54bf7-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="54bf7-114">Чтобы получить интерфейс [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) объекта диспетчера профилей, вызовите функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="54bf7-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="54bf7-115">Чтобы создать пустой профиль, вызовите метод [**ивмпрофилеманажер:: креатимптипрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="54bf7-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="54bf7-116">При создании пустого профиля единственным заданным параметром является версия пакета SDK Windows Media Format, который соответствует профилю.</span><span class="sxs-lookup"><span data-stu-id="54bf7-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="54bf7-117">Если нет особой необходимости использовать предыдущую версию, следует всегда использовать последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="54bf7-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="54bf7-118">Версия определяет структуру профиля; предыдущие версии не поддерживали некоторые свойства.</span><span class="sxs-lookup"><span data-stu-id="54bf7-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="54bf7-119">В следующем примере кода показано, как создать новый профиль.</span><span class="sxs-lookup"><span data-stu-id="54bf7-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="54bf7-120">Чтобы скомпилировать этот код в приложении, включите stdio. h.</span><span class="sxs-lookup"><span data-stu-id="54bf7-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="54bf7-121">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="54bf7-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="54bf7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="54bf7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54bf7-123">**Интерфейс Ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="54bf7-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="54bf7-124">**Интерфейс Ивмпрофилеманажер**</span><span class="sxs-lookup"><span data-stu-id="54bf7-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="54bf7-125">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="54bf7-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 





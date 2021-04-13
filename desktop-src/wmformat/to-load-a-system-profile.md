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
# <a name="to-load-a-system-profile"></a>Загрузка системного профиля

Чтобы внести изменения в системный профиль, необходимо загрузить его в объект профиля. Диспетчер профилей предоставляет два варианта загрузки системных профилей: по идентификатору и по индексу.

Идентификатор системного профиля — это значение GUID, назначенное системному профилю при его создании. Список констант GUID, связанных с системными профилями версии 8, см. в разделе [системные профили](system-profiles.md). Константы GUID для предыдущих версий можно найти в файле заголовка Вмсиспрф. h. Дополнительные сведения об этом и других файлах заголовков, входящих в состав пакета SDK Windows Media Format, см. в разделе [файлы библиотек и параметры компилятора](library-files-and-compiler-settings.md).

В следующем примере кода показано, как загрузить системный профиль с помощью идентификатора системного профиля. Чтобы этот код работал, необходимо включить Вмсиспрф. h и stdio. h. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


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



Если вы не уверены, какой профиль вы хотите использовать, можно выполнить итерацию по всем системным профилям определенной версии с помощью методов [**жетсистемпрофилекаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) и [**лоадсистемпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) интерфейса [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . В каждый момент времени эти методы работают только с одной версией системных профилей. Дополнительные сведения об изменении версии системного профиля см. в разделе [изменение версий системного профиля](to-change-system-profile-versions.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование системных профилей**](using-system-profiles.md)
</dt> </dl>

 

 





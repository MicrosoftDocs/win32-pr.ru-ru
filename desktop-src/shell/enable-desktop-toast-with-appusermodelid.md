---
description: В этом разделе показано, как создать ярлык для приложения, назначить ему AppUserModelID и установить его на начальном экране.
title: Включение всплывающих уведомлений рабочего стола через AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985088"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="f02a1-103">Включение всплывающих уведомлений рабочего стола через AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="f02a1-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="f02a1-104">В этом разделе показано, как создать ярлык для приложения, назначить ему [AppUserModelID](appids.md)и установить его на начальном экране.</span><span class="sxs-lookup"><span data-stu-id="f02a1-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="f02a1-105">Настоятельно рекомендуется делать это в установщик Windows, а не в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="f02a1-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="f02a1-106">Если на начальном экране или во **всех программах** не установлен допустимый ярлык, вы не сможете создавать всплывающие уведомления из классического приложения.</span><span class="sxs-lookup"><span data-stu-id="f02a1-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="f02a1-107">Примеры методов, используемых в этом разделе, взяты из [примера всплывающего уведомления на рабочем столе](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span><span class="sxs-lookup"><span data-stu-id="f02a1-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="f02a1-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="f02a1-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f02a1-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="f02a1-109">Technologies</span></span>

-   <span data-ttu-id="f02a1-110">COM</span><span class="sxs-lookup"><span data-stu-id="f02a1-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f02a1-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f02a1-111">Prerequisites</span></span>

-   <span data-ttu-id="f02a1-112">Библиотеки</span><span class="sxs-lookup"><span data-stu-id="f02a1-112">Libraries</span></span>
    -   <span data-ttu-id="f02a1-113">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="f02a1-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="f02a1-114">C \# : Windows. winmd</span><span class="sxs-lookup"><span data-stu-id="f02a1-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="f02a1-115">В \# . пакет кода Windows API для Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f02a1-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="f02a1-116">Версия Microsoft Visual Studio, поддерживающая не менее Windows 8</span><span class="sxs-lookup"><span data-stu-id="f02a1-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="f02a1-117">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f02a1-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="f02a1-118">Шаг 1. Подготовка ярлыка для создания</span><span class="sxs-lookup"><span data-stu-id="f02a1-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="f02a1-119">В этом примере сначала определяется путь к папке данных приложения пользователя с помощью функции [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) .</span><span class="sxs-lookup"><span data-stu-id="f02a1-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="f02a1-120">Затем он формирует полный путь к ярлыку, определяет, что ярлык этого имени еще не существует в этом расположении, и передает эту информацию другому методу, который создает и устанавливает ярлык.</span><span class="sxs-lookup"><span data-stu-id="f02a1-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="f02a1-121">Обратите внимание, что ярлык можно развернуть для каждого пользователя или для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="f02a1-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="f02a1-122">Шаг 2. Создание ярлыка и его установка на начальном экране</span><span class="sxs-lookup"><span data-stu-id="f02a1-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="f02a1-123">В этом примере также извлекается хранилище свойств ярлыка и задается требуемое свойство [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) из ранее определенной переменной `AppID` .</span><span class="sxs-lookup"><span data-stu-id="f02a1-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="f02a1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="f02a1-124">Remarks</span></span>

<span data-ttu-id="f02a1-125">В качестве альтернативы подходу, приведенному в этом разделе, можно использовать платформу, такую как установщик Windows XML (WiX), для создания ярлыка и его развертывания в составе установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="f02a1-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="f02a1-126">В этом случае этот код следует включать в MSI, а не в код приложения.</span><span class="sxs-lookup"><span data-stu-id="f02a1-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="f02a1-127">Дополнительные сведения см. в примере файла конфигурации WiX, входящего в состав примера " [Отправка всплывающих уведомлений из классических приложений](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) ".</span><span class="sxs-lookup"><span data-stu-id="f02a1-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f02a1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f02a1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f02a1-129">Краткое руководство. отправка всплывающего уведомления с рабочего стола</span><span class="sxs-lookup"><span data-stu-id="f02a1-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="f02a1-130">[Отправка всплывающих уведомлений из примера классического приложения](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="f02a1-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="f02a1-131">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="f02a1-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="f02a1-132">[Руководство. Установка средств установщик Windows XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="f02a1-133">XML-схема всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="f02a1-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="f02a1-134">[Обзор всплывающих уведомлений](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="f02a1-135">[Краткое руководство. отправка всплывающего уведомления](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="f02a1-136">[Краткое руководство. отправка всплывающего push-уведомления](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="f02a1-137">Рекомендации и контрольный список для всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="f02a1-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="f02a1-138">Добавление изображений в шаблон всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="f02a1-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="f02a1-139">Проверка параметров всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="f02a1-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="f02a1-140">[Выбор и использование шаблона всплывающих уведомлений](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="f02a1-141">[Как выполнять активацию с помощью всплывающего уведомления](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="f02a1-142">[Как принять участие в всплывающих уведомлениях](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="f02a1-143">[Выбор шаблона всплывающего уведомления](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="f02a1-144">[Параметры звука всплывающего уведомления](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f02a1-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 

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
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Включение всплывающих уведомлений рабочего стола через AppUserModelID

В этом разделе показано, как создать ярлык для приложения, назначить ему [AppUserModelID](appids.md)и установить его на начальном экране. Настоятельно рекомендуется делать это в установщик Windows, а не в коде приложения. Если на начальном экране или во **всех программах** не установлен допустимый ярлык, вы не сможете создавать всплывающие уведомления из классического приложения.

> [!Note]  
> Примеры методов, используемых в этом разделе, взяты из [примера всплывающего уведомления на рабочем столе](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).

 

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   COM

### <a name="prerequisites"></a>Предварительные условия

-   Библиотеки
    -   C++: Runtime. Object. lib
    -   C \# : Windows. winmd
-   В \# . пакет кода Windows API для Microsoft .NET Framework
-   Версия Microsoft Visual Studio, поддерживающая не менее Windows 8

## <a name="instructions"></a>Инструкции

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Шаг 1. Подготовка ярлыка для создания

В этом примере сначала определяется путь к папке данных приложения пользователя с помощью функции [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) . Затем он формирует полный путь к ярлыку, определяет, что ярлык этого имени еще не существует в этом расположении, и передает эту информацию другому методу, который создает и устанавливает ярлык.

Обратите внимание, что ярлык можно развернуть для каждого пользователя или для каждого приложения.


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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Шаг 2. Создание ярлыка и его установка на начальном экране

В этом примере также извлекается хранилище свойств ярлыка и задается требуемое свойство [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) из ранее определенной переменной `AppID` .


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



## <a name="remarks"></a>Примечания

В качестве альтернативы подходу, приведенному в этом разделе, можно использовать платформу, такую как установщик Windows XML (WiX), для создания ярлыка и его развертывания в составе установщик Windows. В этом случае этот код следует включать в MSI, а не в код приложения. Дополнительные сведения см. в примере файла конфигурации WiX, входящего в состав примера " [Отправка всплывающих уведомлений из классических приложений](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) ".

## <a name="related-topics"></a>См. также

<dl> <dt>

[Краткое руководство. отправка всплывающего уведомления с рабочего стола](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Отправка всплывающих уведомлений из примера классического приложения](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[Идентификаторы модели пользователя приложения (Аппусермоделидс)](appids.md)
</dt> <dt>

[Руководство. Установка средств установщик Windows XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[XML-схема всплывающих уведомлений](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Обзор всплывающих уведомлений](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Краткое руководство. отправка всплывающего уведомления](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Краткое руководство. отправка всплывающего push-уведомления](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Рекомендации и контрольный список для всплывающих уведомлений](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Добавление изображений в шаблон всплывающих уведомлений](/previous-versions/windows/)
</dt> <dt>

[Проверка параметров всплывающих уведомлений](/previous-versions/windows/)
</dt> <dt>

[Выбор и использование шаблона всплывающих уведомлений](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Как выполнять активацию с помощью всплывающего уведомления](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Как принять участие в всплывающих уведомлениях](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Выбор шаблона всплывающего уведомления](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Параметры звука всплывающего уведомления](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 

---
title: Аудитория разработчика и пример кода
description: В этом разделе описываются группы разработчиков, для которых предназначен интерфейс проверки наличия вредоносных программ.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 4ac11c75d5714d0706bed28264f9fa1bf03432af82107826178007e2c42243c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579914"
---
# <a name="developer-audience-and-sample-code"></a>Аудитория разработчика и пример кода

Интерфейс проверки наличия вредоносных программ предназначен для использования двумя группами разработчиков.

- Разработчики приложений, желающие выполнять запросы к антивредоносным продуктам из своих приложений.
- Сторонние создатели продуктов для защиты от вредоносных программ, которые хотят, чтобы их продукты предлагали лучшие функции для приложений.

## <a name="application-developers"></a>Разработчики приложений

AMSI разработан специально для борьбы с вредоносными программами, которые не имеют файлов. типы приложений, которые могут оптимально использовать технологию AMSI, включают в себя обработчики сценариев, приложения, которым требуются буферы памяти для проверки перед их использованием, а также приложения, обрабатывающие файлы, которые могут содержать исполняемый код, отличный от PE (например, Microsoft Word и Excel макросы или документы PDF). Однако полезность технологии AMSI не ограничивается этими примерами.

Существует два способа взаимодействия с AMSI в приложении.

- С помощью API-интерфейсов Win32 AMSI. См. раздел [функции интерфейса проверки на наличие вредоносных программ (AMSI)](/windows/desktop/amsi/antimalware-scan-interface-functions).
- С помощью интерфейсов COM AMSI. См. раздел [интерфейс **иамсистреам**](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Пример кода, демонстрирующий использование AMSI в приложении COM, см. в [примере приложения интерфейса иамсистреам](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Сторонние создатели продуктов для защиты от вредоносных программ

В качестве создателя продуктов для защиты от вредоносных программ можно создать и зарегистрировать собственный внутрипроцессный COM-сервер (DLL) для работы в качестве поставщика AMSI. Этот поставщик AMSI должен реализовывать интерфейс [ **иантималварепровидер**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), и он должен выполняться в процессе.

обратите внимание, что после Windows 10 версии 1709 (обновление для создателя 2017) библиотека DLL поставщика AMSI может не работать, если она зависит от других библиотек dll в пути для загрузки в то же время. Чтобы предотвратить перехват DLL-файлов, рекомендуется, чтобы библиотека DLL поставщика загружала свои зависимости явным образом (с полным путем), используя вызовы безопасного вызова [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) или аналогичные. Мы советуем использовать это вместо того, чтобы полагаться на поведение поиска **LoadLibrary** .

В разделе ниже показано, как зарегистрировать поставщик AMSI. Полный пример кода, демонстрирующий создание библиотеки DLL поставщика AMSI, см. в [примере приложения интерфейса иантималварепровидер](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Регистрация библиотеки DLL поставщика с помощью AMSI

для начала необходимо убедиться, что эти Windows разделы реестра существуют.

- хклм\софтваре\микрософт\амси\провидерс
- хклм\софтваре\классес\клсид

Поставщик AMSI — это внутрипроцессный COM-сервер. Следовательно, он должен зарегистрироваться в модели COM. Классы COM регистрируются в `HKLM\SOFTWARE\Classes\CLSID` .

В приведенном ниже коде показано, как зарегистрировать поставщик AMSI, чей GUID (в нашем примере) предполагается `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

если ваша библиотека DLL реализует [функцию DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), как показано в приведенном выше примере, можно зарегистрировать ее с помощью исполняемого файла, предоставленного Windows `regsvr32.exe` . В командной строке с повышенными привилегиями выполните команду этой формы.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

В этом примере команда создает следующие записи.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**Параметры    REG_SZ пример реализации поставщика AMSI**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**Параметры    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ**

Помимо обычной регистрации COM, необходимо также зарегистрировать поставщик с помощью AMSI. Это можно сделать, добавив запись в следующий раздел.

**хклм\софтваре\микрософт\амси\провидерс**

Например,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

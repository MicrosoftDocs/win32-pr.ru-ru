---
title: Аудитория разработчика и пример кода
description: В этом разделе описываются группы разработчиков, для которых предназначен интерфейс проверки наличия вредоносных программ.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2020
ms.locfileid: "104069491"
---
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="156f5-103">Аудитория разработчика и пример кода</span><span class="sxs-lookup"><span data-stu-id="156f5-103">Developer audience, and sample code</span></span>

<span data-ttu-id="156f5-104">Интерфейс проверки наличия вредоносных программ предназначен для использования двумя группами разработчиков.</span><span class="sxs-lookup"><span data-stu-id="156f5-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="156f5-105">Разработчики приложений, желающие выполнять запросы к антивредоносным продуктам из своих приложений.</span><span class="sxs-lookup"><span data-stu-id="156f5-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="156f5-106">Сторонние создатели продуктов для защиты от вредоносных программ, которые хотят, чтобы их продукты предлагали лучшие функции для приложений.</span><span class="sxs-lookup"><span data-stu-id="156f5-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="156f5-107">Разработчики приложений</span><span class="sxs-lookup"><span data-stu-id="156f5-107">Application developers</span></span>

<span data-ttu-id="156f5-108">AMSI разработан специально для борьбы с вредоносными программами, которые не имеют файлов.</span><span class="sxs-lookup"><span data-stu-id="156f5-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="156f5-109">Типы приложений, которые могут оптимально использовать технологию AMSI, включают в себя обработчики сценариев, приложения, которым требуются буферы памяти для проверки перед их использованием, а также приложения, обрабатывающие файлы, которые могут содержать исполняемый код, отличный от PE (например, макросы Microsoft Word и Excel или документы PDF).</span><span class="sxs-lookup"><span data-stu-id="156f5-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="156f5-110">Однако полезность технологии AMSI не ограничивается этими примерами.</span><span class="sxs-lookup"><span data-stu-id="156f5-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="156f5-111">Существует два способа взаимодействия с AMSI в приложении.</span><span class="sxs-lookup"><span data-stu-id="156f5-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="156f5-112">С помощью API-интерфейсов Win32 AMSI.</span><span class="sxs-lookup"><span data-stu-id="156f5-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="156f5-113">См. раздел [функции интерфейса проверки на наличие вредоносных программ (AMSI)](/windows/desktop/amsi/antimalware-scan-interface-functions).</span><span class="sxs-lookup"><span data-stu-id="156f5-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="156f5-114">С помощью интерфейсов COM AMSI.</span><span class="sxs-lookup"><span data-stu-id="156f5-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="156f5-115">См. раздел [интерфейс **иамсистреам**](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span><span class="sxs-lookup"><span data-stu-id="156f5-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="156f5-116">Пример кода, демонстрирующий использование AMSI в приложении COM, см. в [примере приложения интерфейса иамсистреам](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span><span class="sxs-lookup"><span data-stu-id="156f5-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="156f5-117">Сторонние создатели продуктов для защиты от вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="156f5-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="156f5-118">В качестве создателя продуктов для защиты от вредоносных программ можно создать и зарегистрировать собственный внутрипроцессный COM-сервер (DLL) для работы в качестве поставщика AMSI.</span><span class="sxs-lookup"><span data-stu-id="156f5-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="156f5-119">Этот поставщик AMSI должен реализовывать интерфейс [ **иантималварепровидер**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), и он должен выполняться в процессе.</span><span class="sxs-lookup"><span data-stu-id="156f5-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="156f5-120">Обратите внимание, что после Windows 10, версия 1709 (обновление для создателя 2017), Библиотека DLL поставщика AMSI может не работать, если она зависит от других библиотек DLL в пути для загрузки в то же время.</span><span class="sxs-lookup"><span data-stu-id="156f5-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="156f5-121">Чтобы предотвратить перехват DLL-файлов, рекомендуется, чтобы библиотека DLL поставщика загружала свои зависимости явным образом (с полным путем), используя вызовы безопасного вызова [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) или аналогичные.</span><span class="sxs-lookup"><span data-stu-id="156f5-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="156f5-122">Мы советуем использовать это вместо того, чтобы полагаться на поведение поиска **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="156f5-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="156f5-123">В разделе ниже показано, как зарегистрировать поставщик AMSI.</span><span class="sxs-lookup"><span data-stu-id="156f5-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="156f5-124">Полный пример кода, демонстрирующий создание библиотеки DLL поставщика AMSI, см. в [примере приложения интерфейса иантималварепровидер](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span><span class="sxs-lookup"><span data-stu-id="156f5-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="156f5-125">Регистрация библиотеки DLL поставщика с помощью AMSI</span><span class="sxs-lookup"><span data-stu-id="156f5-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="156f5-126">Для начала необходимо убедиться, что эти разделы реестра Windows существуют.</span><span class="sxs-lookup"><span data-stu-id="156f5-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="156f5-127">хклм\софтваре\микрософт\амси\провидерс</span><span class="sxs-lookup"><span data-stu-id="156f5-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="156f5-128">хклм\софтваре\классес\клсид</span><span class="sxs-lookup"><span data-stu-id="156f5-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="156f5-129">Поставщик AMSI — это внутрипроцессный COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="156f5-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="156f5-130">Следовательно, он должен зарегистрироваться в модели COM.</span><span class="sxs-lookup"><span data-stu-id="156f5-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="156f5-131">Классы COM регистрируются в `HKLM\SOFTWARE\Classes\CLSID` .</span><span class="sxs-lookup"><span data-stu-id="156f5-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="156f5-132">В приведенном ниже коде показано, как зарегистрировать поставщик AMSI, чей GUID (в нашем примере) предполагается `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .</span><span class="sxs-lookup"><span data-stu-id="156f5-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

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

<span data-ttu-id="156f5-133">Если в библиотеке DLL реализована [Функция DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), как показано в приведенном выше примере, можно зарегистрировать ее с помощью исполняемого файла, предоставленного Windows `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="156f5-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="156f5-134">В командной строке с повышенными привилегиями выполните команду этой формы.</span><span class="sxs-lookup"><span data-stu-id="156f5-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="156f5-135">В этом примере команда создает следующие записи.</span><span class="sxs-lookup"><span data-stu-id="156f5-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="156f5-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="156f5-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="156f5-137">&nbsp;&nbsp;&nbsp;&nbsp;**Параметры    REG_SZ пример реализации поставщика AMSI**</span><span class="sxs-lookup"><span data-stu-id="156f5-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="156f5-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="156f5-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="156f5-139">&nbsp;&nbsp;&nbsp;&nbsp;**Параметры    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="156f5-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="156f5-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ**</span><span class="sxs-lookup"><span data-stu-id="156f5-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="156f5-141">Помимо обычной регистрации COM, необходимо также зарегистрировать поставщик с помощью AMSI.</span><span class="sxs-lookup"><span data-stu-id="156f5-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="156f5-142">Это можно сделать, добавив запись в следующий раздел.</span><span class="sxs-lookup"><span data-stu-id="156f5-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="156f5-143">**хклм\софтваре\микрософт\амси\провидерс**</span><span class="sxs-lookup"><span data-stu-id="156f5-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="156f5-144">Например,</span><span class="sxs-lookup"><span data-stu-id="156f5-144">For example,</span></span>

<span data-ttu-id="156f5-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="156f5-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

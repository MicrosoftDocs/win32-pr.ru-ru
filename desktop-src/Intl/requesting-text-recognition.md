---
description: Запрос распознавания текста
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: Запрос распознавания текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2442cfa1e26185c4c8d882fe71bb178911f4d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682624"
---
# <a name="requesting-text-recognition"></a><span data-ttu-id="f6107-103">Запрос распознавания текста</span><span class="sxs-lookup"><span data-stu-id="f6107-103">Requesting Text Recognition</span></span>

<span data-ttu-id="f6107-104">Приложение вызывает функцию [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) для запроса распознавания текста из определенной службы ELS.</span><span class="sxs-lookup"><span data-stu-id="f6107-104">The application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to request text recognition from a specific ELS service.</span></span> <span data-ttu-id="f6107-105">Служба должна быть обнаружена в предыдущем вызове [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), как описано в разделе [**перечисление и освобождение служб**](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="f6107-105">The service must have been discovered in a previous call to [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), as described in [**Enumerating and Freeing Services**](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="f6107-106">Платформа может обрабатывать вызовы [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f6107-106">The platform can process [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) calls either synchronously or asynchronously.</span></span>

 

<span data-ttu-id="f6107-107">[**Маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) обрабатывает следующие типы текста:</span><span class="sxs-lookup"><span data-stu-id="f6107-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) handles the following types of text:</span></span>

-   <span data-ttu-id="f6107-108">Обнаружение языка Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f6107-108">Microsoft language detection.</span></span> <span data-ttu-id="f6107-109">UTF-16, форма нормализации C, текст, для которого определяется язык.</span><span class="sxs-lookup"><span data-stu-id="f6107-109">UTF-16, normalization form C, text for which to determine the language.</span></span>
-   <span data-ttu-id="f6107-110">Обнаружение сценариев Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f6107-110">Microsoft script detection.</span></span> <span data-ttu-id="f6107-111">Текст UTF-16, для которого необходимо определить диапазоны скриптов.</span><span class="sxs-lookup"><span data-stu-id="f6107-111">UTF-16 text for which to determine script ranges.</span></span>
-   <span data-ttu-id="f6107-112">Службы транслитерации.</span><span class="sxs-lookup"><span data-stu-id="f6107-112">Transliteration services.</span></span> <span data-ttu-id="f6107-113">Текст в кодировке UTF-16, написанный в исходном скрипте (система записи).</span><span class="sxs-lookup"><span data-stu-id="f6107-113">UTF-16 text written in source script (writing system).</span></span>

## <a name="use-synchronous-text-recognition"></a><span data-ttu-id="f6107-114">Использовать синхронное распознавание текста</span><span class="sxs-lookup"><span data-stu-id="f6107-114">Use Synchronous Text Recognition</span></span>

<span data-ttu-id="f6107-115">В этом разделе приводятся инструкции по нескольким способам выполнения синхронного распознавания текста.</span><span class="sxs-lookup"><span data-stu-id="f6107-115">This section provides instructions for several ways to perform synchronous text recognition.</span></span>

<span data-ttu-id="f6107-116">**Синхронное распознавание текста с помощью службы Microsoft распознавание языка**</span><span class="sxs-lookup"><span data-stu-id="f6107-116">**Synchronous Text Recognition with Microsoft Language Detection Service**</span></span>

<span data-ttu-id="f6107-117">В следующем примере показано использование [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) со службой Microsoft распознавание языка и вывод всех результатов, полученных службой.</span><span class="sxs-lookup"><span data-stu-id="f6107-117">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Language Detection service, and prints all the results retrieved by the service.</span></span> <span data-ttu-id="f6107-118">Формат вывода этой службы — это единая структура [**\_ \_ диапазона данных сопоставления**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) с элементом **pData** , указывающим на массив строк в формате Юникода, заканчивающийся двойным нулем,</span><span class="sxs-lookup"><span data-stu-id="f6107-118">The output format of this service is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to a Unicode double-null-terminated, registry-formatted array of strings.</span></span> <span data-ttu-id="f6107-119">Каждая строка массива завершается нулем, а для указания конца массива используется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f6107-119">Every string of the array is null-terminated and an empty string is used to specify the end of the array.</span></span> <span data-ttu-id="f6107-120">Содержимое массива — это имена языков, отсортированные по достоверности.</span><span class="sxs-lookup"><span data-stu-id="f6107-120">The contents of the array are language names sorted by confidence.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    WCHAR * p;

    // The return format of the Language Auto-Detection is a
    // double null-terminated registry-formatted array of strings.
    // Every string of the array is null-terminated and there's an
    // empty string specifying the end of the array.
    for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
    {
        printf("%ws\n", p);
    }
}
```



<span data-ttu-id="f6107-121">**Синхронное распознавание текста со службой обнаружения сценариев (Майкрософт)**</span><span class="sxs-lookup"><span data-stu-id="f6107-121">**Synchronous Text Recognition with Microsoft Script Detection Service**</span></span>

<span data-ttu-id="f6107-122">В следующем примере показано использование [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) со службой обнаружения скриптов Майкрософт и вывод всех полученных результатов.</span><span class="sxs-lookup"><span data-stu-id="f6107-122">The next example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Script Detection service, and prints all the retrieved results.</span></span> <span data-ttu-id="f6107-123">Формат вывода этой службы — это массив структур [**\_ \_ диапазона данных сопоставления**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) , каждый из которых указывает текст, написанный в том же скрипте.</span><span class="sxs-lookup"><span data-stu-id="f6107-123">The output format of this service is an array of [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structures, each specifying text written in the same script.</span></span> <span data-ttu-id="f6107-124">Общие (Зиии) символы добавляются к предыдущему диапазону или к следующему диапазону, если предыдущий диапазон не существует.</span><span class="sxs-lookup"><span data-stu-id="f6107-124">Common (Zyyy) characters are added to the previous range, or to the next range if the previous range does not exist.</span></span> <span data-ttu-id="f6107-125">Элемент **pData** каждой структуры указывает на строку в Юникоде, заканчивающуюся нулем, которая содержит стандартное имя скрипта в Юникоде для определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="f6107-125">The **pData** member of each structure points to a Unicode null-terminated string containing the standard Unicode name of the script for the particular range.</span></span>

> [!Note]  
> <span data-ttu-id="f6107-126">Начиная с Windows 7, служба обнаружения сценариев Майкрософт соответствует Юникоду 5,1.</span><span class="sxs-lookup"><span data-stu-id="f6107-126">As of Windows 7, the Microsoft Script Detection service complies with Unicode 5.1.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Script Detection GUID to enumerate SD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_SCRIPT_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData);
    }
}
```



<span data-ttu-id="f6107-127">**Синхронное распознавание текста с помощью службы транслитерации Microsoft кириллицы и латиницы**</span><span class="sxs-lookup"><span data-stu-id="f6107-127">**Synchronous Text Recognition with Microsoft Cyrillic to Latin Transliteration Service**</span></span>

<span data-ttu-id="f6107-128">В следующем примере показано использование [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) со службой Microsoft кириллицы to Latin транслитерации и вывод полученных результатов.</span><span class="sxs-lookup"><span data-stu-id="f6107-128">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Cyrillic to Latin transliteration service, and prints the retrieved results.</span></span> <span data-ttu-id="f6107-129">Обратите внимание на два разных способа перечисления этой службы: по GUID или по категориям и входным сценариям.</span><span class="sxs-lookup"><span data-stu-id="f6107-129">Note the two different ways to enumerate this service, either by GUID or by category and input script.</span></span>

<span data-ttu-id="f6107-130">Формат выходных данных одинаков для всех доступных служб транслитерации.</span><span class="sxs-lookup"><span data-stu-id="f6107-130">The output format is the same for all available transliteration services.</span></span> <span data-ttu-id="f6107-131">Это единая структура [**\_ \_ диапазона данных сопоставления**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) с элементом **pData** , указывающим на массив символов Юникода, представляющий исходный текст, преобразованный в выходной скрипт, применяя только правила конкретной службы транслитерации.</span><span class="sxs-lookup"><span data-stu-id="f6107-131">It is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to an array of Unicode characters representing the original text transliterated into the output script by applying only the rules of the specific transliteration service.</span></span> <span data-ttu-id="f6107-132">Эта служба не имеет значения NULL — завершает свои выходные данные, если входные данные не содержат завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="f6107-132">This service does not null-terminate its output if the input does not contain the terminating null character.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT (L"Skip The russian word for 'yes' is transliterated to Latin as '\x0434\x0430'.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices;
    DWORD                   dwServicesCount;
    HRESULT                 hResult;

    // 1. Enumerate by GUID:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Use the Cyrl->Latn Transliteration GUID to enumerate only this service:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    printf("--\n");

    // 2. Enumerate by input script and category:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    EnumOptions.pszCategory = L"Transliteration";
    EnumOptions.pszInputScript = L"Cyrl";
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    // We want the result to be null-terminated for display.
    // That's why we will also pass the input null terminator:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT) + 1, USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[0].pData);
}
```



<span data-ttu-id="f6107-133">**Синхронное распознавание текста с помощью вызова всех доступных служб**</span><span class="sxs-lookup"><span data-stu-id="f6107-133">**Synchronous Text Recognition with a Call to All Available Services**</span></span>

<span data-ttu-id="f6107-134">В следующем примере показано использование [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) со всеми доступными службами и вывод полученных результатов для всех служб.</span><span class="sxs-lookup"><span data-stu-id="f6107-134">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with all available services, and prints the retrieved results for all the services.</span></span> <span data-ttu-id="f6107-135">В этом примере приведена хорошая иллюстрация работы каждой службы.</span><span class="sxs-lookup"><span data-stu-id="f6107-135">This example provides a good illustration of the operation of each service.</span></span> <span data-ttu-id="f6107-136">Просматривая выходные данные примера приложения, можно легко определить, что происходит внутри служб.</span><span class="sxs-lookup"><span data-stu-id="f6107-136">By looking at the output of the example application, it is easy to find out what is happening internally with the services.</span></span> <span data-ttu-id="f6107-137">В этом примере также показано, что почти весь код, используемый для вызова любой из ELS служб, одинаков.</span><span class="sxs-lookup"><span data-stu-id="f6107-137">This example also shows that almost all code used to call any of the ELS services is the same.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    DWORD i;

    // Get all installed ELS services:
    hResult = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service:
            // ... prgServices[i] ...
            if (i > 0)
            {
                printf("--\n");
            }
            hResult = CallMappingRecognizeText(&prgServices[i]);
            if (SUCCEEDED(hResult))
            {
                printf("Calling the service %ws has succeeded!\n",
                    prgServices[i].pszDescription);
            }
            else
            {
                printf("Calling the service %ws has failed, failure = 0x%x!\n",
                    prgServices[i].pszDescription, hResult);
            }
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;
    DWORD dwDataIndex;
    WCHAR c;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        // Currently, we can treat all results as arrays of unicode WCHAR
        // characters, but there can be services in the future
        // that use different formatting, i.e. XML, HTML, etc.
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"");
        for (dwDataIndex = 0; dwDataIndex < pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2; ++dwDataIndex)
        {
            c = ((WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData)[dwDataIndex];
            if (c >= 32 && c < 128 && c != '"') printf("%wc", c);
            else printf("#%x", (unsigned)c);
        }
        printf("\"\n");
    }
}

void CallRecognizeText(LPCWSTR Category, LPCWSTR Text)
{
    HRESULT               Result;
    PMAPPING_SERVICE_INFO rgServices;
    DWORD                 ServicesCount;
    MAPPING_ENUM_OPTIONS  options = {sizeof(MAPPING_ENUM_OPTIONS), (LPWSTR) Category, 0};

    Result = MappingGetServices(&options, &rgServices, &ServicesCount);
    if (Result == S_OK && ServicesCount > 0)
    {
        MAPPING_PROPERTY_BAG bag = { sizeof(MAPPING_PROPERTY_BAG), 0};
        Result = MappingRecognizeText(&rgServices[0], Text, wcslen(Text), 0, NULL, &bag);
        if (Result == S_OK)
        {
            MappingFreePropertyBag(&bag);
        }

        MappingFreeServices(rgServices);
    }
}
int _tmain(int argc, _TCHAR* argv[])
{
    CallRecognizeText(L"Language Detection", L"Text to be recognized");
  
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    return 0;
}
```



## <a name="use-asynchronous-text-recognition"></a><span data-ttu-id="f6107-138">Использовать асинхронное распознавание текста</span><span class="sxs-lookup"><span data-stu-id="f6107-138">Use Asynchronous Text Recognition</span></span>

<span data-ttu-id="f6107-139">В следующем примере показано использование [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) для асинхронного распознавания текста.</span><span class="sxs-lookup"><span data-stu-id="f6107-139">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) for asynchronous text recognition.</span></span> <span data-ttu-id="f6107-140">При использовании обратного вызова приложение должно убедиться, что контейнер свойств, входной текст, параметры и служба действительны до завершения выполнения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f6107-140">When the callback is used, the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback has finished executing.</span></span>

<span data-ttu-id="f6107-141">Приложение должно вызвать [**маппингфрипропертибаг**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) сразу после того, как контейнер будет использован функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f6107-141">The application must call [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) immediately after the bag is consumed by the callback function.</span></span> <span data-ttu-id="f6107-142">Дополнительные сведения см. в разделе [предоставление обратных вызовов для служб ELS Services](providing-callbacks-for-els-services.md).</span><span class="sxs-lookup"><span data-stu-id="f6107-142">For more information, see [Providing Callbacks for ELS Services](providing-callbacks-for-els-services.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG    bag;
    MAPPING_OPTIONS         Options;
    HRESULT                 hResult;
    HANDLE                  SyncEvent;
    DWORD                   dwWaitResult;

    SyncEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (SyncEvent == NULL)
    {
        hResult = E_FAIL;
    }
    else
    {
        ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
        bag.Size = sizeof (MAPPING_PROPERTY_BAG);

        ZeroMemory(&Options, sizeof (MAPPING_OPTIONS));
        Options.Size = sizeof (MAPPING_OPTIONS);
        Options.pfnRecognizeCallback = (PFN_MAPPINGCALLBACKPROC)RecognizeCallback;
        Options.pRecognizeCallerData = &SyncEvent;
        Options.dwRecognizeCallerDataSize = sizeof (HANDLE);

        // MappingRecognizeText's dwIndex parameter specifies the first
        // index inside the text from where the recognition should start.
        // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
        // of the input string.
        hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, &Options, &bag);
        if (SUCCEEDED(hResult))
        {
            // We are using an event to synchronize our waiting for the call to end,
            // because some objects have to be valid till the end of the callback call:
            // - the input text
            // - the property bag
            // - the options
            // - the service
            dwWaitResult = WaitForSingleObject(SyncEvent, INFINITE);
            if (dwWaitResult != WAIT_OBJECT_0)
            {
                hResult = E_FAIL;
            }
        }
        CloseHandle(SyncEvent);
    }
    return hResult;
}

void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result)
{
    HANDLE SyncEvent;
    WCHAR * p;

    UNREFERENCED_PARAMETER(dwDataSize);

    if (SUCCEEDED(Result))
    {
        for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
        {
            printf("%ws\n", p);
        }
        MappingFreePropertyBag(pBag);
    }

    SyncEvent = *((HANDLE *)data);
    SetEvent(SyncEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="f6107-143">См. также</span><span class="sxs-lookup"><span data-stu-id="f6107-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6107-144">Использование расширенных лингвистических служб</span><span class="sxs-lookup"><span data-stu-id="f6107-144">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="f6107-145">Предоставление обратных вызовов для служб ELS Services</span><span class="sxs-lookup"><span data-stu-id="f6107-145">Providing Callbacks for ELS Services</span></span>](providing-callbacks-for-els-services.md)
</dt> <dt>

[<span data-ttu-id="f6107-146">**маппингфрипропертибаг**</span><span class="sxs-lookup"><span data-stu-id="f6107-146">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="f6107-147">**маппингжетсервицес**</span><span class="sxs-lookup"><span data-stu-id="f6107-147">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[<span data-ttu-id="f6107-148">**маппингрекогнизетекст**</span><span class="sxs-lookup"><span data-stu-id="f6107-148">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 




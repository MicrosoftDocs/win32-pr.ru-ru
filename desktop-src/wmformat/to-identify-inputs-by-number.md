---
title: Для обнаружения входных данных по номеру
description: Для обнаружения входных данных по номеру
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Расширенный формат систем (ASF), идентификация входов по номеру
- ASF (Расширенный системный формат), идентификация входов по номеру
- профили, идентификация входов по номеру
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069557"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="af5f4-106">Для обнаружения входных данных по номеру</span><span class="sxs-lookup"><span data-stu-id="af5f4-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="af5f4-107">Каждый пример, передаваемый в модуль записи, должен быть связан с входным номером.</span><span class="sxs-lookup"><span data-stu-id="af5f4-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="af5f4-108">Каждый входной номер соответствует одному или нескольким потокам в профиле, используемым модулем записи для записи файла.</span><span class="sxs-lookup"><span data-stu-id="af5f4-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="af5f4-109">В профиле источники мультимедиа идентифицируются по имени подключения.</span><span class="sxs-lookup"><span data-stu-id="af5f4-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="af5f4-110">Модуль записи связывает входной номер с каждым именем соединения при настройке профиля для модуля записи.</span><span class="sxs-lookup"><span data-stu-id="af5f4-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="af5f4-111">Прежде чем можно будет передавать образцы в модуль записи, необходимо определить, какие данные будут обрабатываться каждым входным данным.</span><span class="sxs-lookup"><span data-stu-id="af5f4-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="af5f4-112">Нельзя предположить, что входные данные будут находиться в том же порядке, что и потоки в профиле, даже если это часто случается.</span><span class="sxs-lookup"><span data-stu-id="af5f4-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="af5f4-113">Таким образом, единственным надежным способом сопоставления входных данных с потоками является сравнение имени соединения входных данных с именем соединения потока.</span><span class="sxs-lookup"><span data-stu-id="af5f4-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="af5f4-114">Чтобы узнать имена подключений и соответствующие входные номера для загруженного профиля, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="af5f4-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="af5f4-115">Создайте объект модуля записи и задайте профиль для использования.</span><span class="sxs-lookup"><span data-stu-id="af5f4-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="af5f4-116">Дополнительные сведения о настройке профилей в средстве записи см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="af5f4-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="af5f4-117">Необходимо иметь представление о именах соединений, используемых для потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="af5f4-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="af5f4-118">Имя соединения можно получить в профиле путем получения объекта конфигурации потока для каждого потока и вызова [**ивмстреамконфиг:: жетконнектионнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="af5f4-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="af5f4-119">Дополнительные сведения о профилях и объектах конфигурации потоков см. в разделе [Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="af5f4-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="af5f4-120">Получите общее число входов, вызвав [**ивмвритер:: жетинпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span><span class="sxs-lookup"><span data-stu-id="af5f4-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="af5f4-121">Выполните цикл по всем входным данным, выполнив следующие действия для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="af5f4-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="af5f4-122">Получите интерфейс [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) для входных данных, вызвав [**Ивмвритер:: жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="af5f4-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="af5f4-123">Получите имя соединения, соответствующее входному номеру, вызвав [**ивминпутмедиапропс:: жетконнектионнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="af5f4-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="af5f4-124">После получения имени соединения вы узнаете о потоках, связанных с входными номерами, назначенными модулем записи.</span><span class="sxs-lookup"><span data-stu-id="af5f4-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="af5f4-125">В следующем примере кода отображается имя соединения для каждого входного аргумента.</span><span class="sxs-lookup"><span data-stu-id="af5f4-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="af5f4-126">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="af5f4-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="af5f4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="af5f4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af5f4-128">**Интерфейс Ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="af5f4-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="af5f4-129">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="af5f4-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





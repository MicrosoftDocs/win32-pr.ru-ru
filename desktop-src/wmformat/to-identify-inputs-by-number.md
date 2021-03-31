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
# <a name="to-identify-inputs-by-number"></a>Для обнаружения входных данных по номеру

Каждый пример, передаваемый в модуль записи, должен быть связан с входным номером. Каждый входной номер соответствует одному или нескольким потокам в профиле, используемым модулем записи для записи файла. В профиле источники мультимедиа идентифицируются по имени подключения. Модуль записи связывает входной номер с каждым именем соединения при настройке профиля для модуля записи. Прежде чем можно будет передавать образцы в модуль записи, необходимо определить, какие данные будут обрабатываться каждым входным данным. Нельзя предположить, что входные данные будут находиться в том же порядке, что и потоки в профиле, даже если это часто случается. Таким образом, единственным надежным способом сопоставления входных данных с потоками является сравнение имени соединения входных данных с именем соединения потока.

Чтобы узнать имена подключений и соответствующие входные номера для загруженного профиля, выполните следующие действия.

1.  Создайте объект модуля записи и задайте профиль для использования. Дополнительные сведения о настройке профилей в средстве записи см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md). Необходимо иметь представление о именах соединений, используемых для потоков в профиле. Имя соединения можно получить в профиле путем получения объекта конфигурации потока для каждого потока и вызова [**ивмстреамконфиг:: жетконнектионнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname). Дополнительные сведения о профилях и объектах конфигурации потоков см. в разделе [Работа с профилями](working-with-profiles.md).
2.  Получите общее число входов, вызвав [**ивмвритер:: жетинпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).
3.  Выполните цикл по всем входным данным, выполнив следующие действия для каждого из них.
    -   Получите интерфейс [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) для входных данных, вызвав [**Ивмвритер:: жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
    -   Получите имя соединения, соответствующее входному номеру, вызвав [**ивминпутмедиапропс:: жетконнектионнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname). После получения имени соединения вы узнаете о потоках, связанных с входными номерами, назначенными модулем записи.

В следующем примере кода отображается имя соединения для каждого входного аргумента. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 





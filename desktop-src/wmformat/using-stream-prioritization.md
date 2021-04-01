---
title: Использование определения приоритетов потоков
description: Использование определения приоритетов потоков
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Media Format SDK, определение приоритетов потоков
- профили, определение приоритетов потоков
- потоки, определение приоритетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987175"
---
# <a name="using-stream-prioritization"></a>Использование определения приоритетов потоков

Приоритизация потоков позволяет более точно управлять воспроизведением содержимого, позволяя указывать порядок приоритетов для потоков в профиле. Если во время воспроизведения сервер чтения и потоковой передачи столкнулись с нехваткой пропускной способности, может потребоваться удалить примеры, чтобы обеспечить непрерывное воспроизведение. Если указать порядок приоритета с объектом приоритета потока в профиле, примеры будут удалены из потоков с наименьшим приоритетом.

В отличие от совместного использования пропускной способности и объектов взаимного исключения, объект определения приоритетов потоков не использует интерфейс [**ивмстреамлист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) для наблюдения за списком потоков. Вместо этого необходимо использовать массив структур [**\_ \_ \_ записи с приоритетом WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) . Структуры должны быть упорядочены в массиве в порядке убывания приоритета. В дополнение к удержанию номера потока, структура приоритета потока также позволяет указать, является ли поток обязательным. Обязательные потоки не будут удалены, независимо от их расположения в списке.

В следующем примере кода показано, как включить определение приоритетов потоков в профиле. Этот профиль предназначен для презентации в классе с звуковым потоком лекции, видеопотоком лекции и потоком видео, записывающим слайды презентации. Звуковой поток является наиболее важным и будет обязательным. Слайды презентации будут иметь самый низкий приоритет, так как изображение будет довольно постоянным, поэтому здесь будут потеряны несколько рамок, и это не будет существенно отличаться.


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Работа с профилями**](working-with-profiles.md)
</dt> </dl>

 

 





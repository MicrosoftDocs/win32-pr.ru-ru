---
title: Использование маркеров
description: Использование маркеров
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, маркеры
- Расширенный формат систем (ASF), маркеры
- ASF (Расширенный системный формат), маркеры
- Расширенный системный формат (ASF), Поиск маркеров
- ASF (Расширенный системный формат), Поиск маркеров
- маркеры, сведения
- маркеры, добавление
- маркеры, удаление
- маркеры, извлечение
- маркеры, Поиск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789234"
---
# <a name="using-markers"></a>Использование маркеров

*Маркер* — это именованная точка в файле ASF. Каждый маркер состоит из имени и связанного времени, измеряемого как смещение от начала файла. Приложение может использовать маркеры для назначения имен различным точкам внутри содержимого, отображать эти имена пользователю, а затем искать позиции маркеров. Приложение может добавлять или удалять маркеры из существующего файла ASF.

Интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) содержит методы для работы с маркерами. Объект редактора метаданных поддерживает добавление и удаление маркеров. Объекты Writer и Reader могут извлекать маркеры, но не могут добавлять или удалять маркеры.

## <a name="adding-markers"></a>Добавление маркеров

Чтобы добавить маркер, запросите редактор метаданных для интерфейса **ивмхеадеринфо** . Затем вызовите метод [**ивмхеадеринфо:: аддмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , указав имя маркера в виде строки расширенных символов и время в 100-наносекундных единицах. Время не должно превышать длительность файла. Два маркера могут иметь одно и то же время.

В следующем примере в файл добавляется несколько маркеров:


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>Удаление маркеров

Чтобы удалить маркер, вызовите [**ивмхеадеринфо:: ремовемаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), указав индекс удаляемого маркера. Маркеры автоматически сортируются в порядке возрастания времени, поэтому индекс 0 всегда является первым маркером. Обратите внимание, что вызов **ремовемаркер** изменяет номера индексов следующих маркеров. Следующий код, где *пинфо* — это указатель на интерфейс **ивмхеадеринфо** , удаляет все маркеры из файла:


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>Получение маркеров

Чтобы получить имя и время маркера, выполните следующие действия.

1.  Вызовите метод [**ивмхеадеринфо:: жетмаркеркаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) , чтобы определить, сколько маркеров содержит файл.
2.  Получение размера строки, необходимой для хранения имени маркера. Чтобы сделать это, вызовите метод [**ивмхеадеринфо:: @ Mark**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) . Укажите индекс извлекаемого маркера и **значение NULL** для буфера строки (параметр *пвсзмаркернаме* ). Метод возвращает длину строки, включая завершающий \\ символ "0", в параметре *пкчмаркернамелен* .
3.  Выделить строку расширенных символов для получения имени.
4.  Снова  вызовите метод GetString, но в это время передайте адрес строки в параметре *пвсзмаркернаме* . Метод записывает имя маркера в строку и возвращает время метки в параметре *пкнсмаркертиме* .

В следующем коде каждый маркер перебирается по порядку и получает имя и время:


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>Поиск маркера

Чтобы начать воспроизведение из расположения маркера, вызовите метод [**IWMReaderAdvanced2:: стартатмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) объекта Reader, указав индекс маркера. Остальные параметры идентичны параметрам метода [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . В следующем примере производится запрос к модулю чтения для интерфейса [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) и осуществляется поиск первого маркера.


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2:: Стартатмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**Работа с метаданными**](working-with-metadata.md)
</dt> </dl>

 

 





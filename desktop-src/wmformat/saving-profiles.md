---
title: Сохранение профилей
description: Сохранение профилей
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Пакет SDK для формата мультимедиа, сохранение профилей
- Windows Пакет SDK для формата мультимедиа, сохранение профиля
- профили, сохранение
- профили, интерфейс Ивмпрофилеманажер
- Ивмпрофилеманажер, сохранение профилей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6befb09d7e0d628462bdd22e1e905c351be58dc077959089883ce3707dc493d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547044"
---
# <a name="saving-profiles"></a>Сохранение профилей

Можно использовать метод [**ивмпрофилеманажер:: савепрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) , чтобы сохранить содержимое объекта профиля в строку, отформатированную с помощью XML. Для сохранения строки профиля в файл не предоставляются методы. Вы можете использовать подпрограммы файлового ввода-вывода по своему усмотрению.

> [!Note]  
> Никогда не следует изменять строку профиля, записанную в файл. Любые изменения, которые необходимо внести в профиль, следует вносить программно. Изменение значений в пркс-файле может привести к непредсказуемым результатам.

 

В следующем примере показана функция для сохранения профиля в файл с помощью стандартного ввода-вывода файла в стиле C. Чтобы скомпилировать приложение, использующее этот пример, необходимо включить stdio. h в проект.


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Работа с профилями**](working-with-profiles.md)
</dt> </dl>

 

 





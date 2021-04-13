---
title: Сохранение профилей
description: Сохранение профилей
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Media Format SDK, сохранение профилей
- Windows Media Format SDK, сохранение профиля
- профили, сохранение
- профили, интерфейс Ивмпрофилеманажер
- Ивмпрофилеманажер, сохранение профилей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412488"
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Работа с профилями**](working-with-profiles.md)
</dt> </dl>

 

 





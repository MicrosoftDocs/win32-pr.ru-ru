---
title: Воспроизведение ЗВУКовых ресурсов
description: Воспроизведение ЗВУКовых ресурсов
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- звуковая волна, воспроизведение ВОЛНовых ресурсов
- Вспомогательные аудио, воспроизведение ЗВУКовых ресурсов
- Воспроизведение ЗВУКовых ресурсов
- Функция PlaySound, воспроизведение ресурсов WAVE
- Функция Сндплайсаунд
- PlaySound, функция по сравнению с функцией Сндплайсаунд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd256d3c4cf07d6d2f57ba9c4d85c54b9d0e599f9382a5b8d9d1f3a0ef4705ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136763"
---
# <a name="playing-wave-resources"></a>Воспроизведение ЗВУКовых ресурсов

Функцию [**PlaySound**](/previous-versions//dd743680(v=vs.85)) можно использовать для воспроизведения звука, хранящегося в виде ресурса. Хотя это и возможно с помощью функции [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) , **сндплайсаунд** требует поиска, загрузки, блокировки, разблокировки и освобождения ресурса. **PlaySound** все это достигается с помощью одной строки кода.

## <a name="playsound-example"></a>Пример PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Пример Сндплайсаунд

\_Флаг памяти snd указывает, что параметр *лпсзсаунднаме* является указателем на изображение файла Wave в памяти. Чтобы включить файл WAVE в качестве ресурса в приложение, добавьте следующую запись в скрипт ресурсов приложения (. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



Имя *саунднаме* — это заполнитель для имени, которое указывается для ссылки на этот ресурс. ресурсы WAVE загружаются и доступны так же, как и другие ресурсы, определяемые приложением Windows. Функция Плайресаурце в следующем примере воспроизводит указанный ресурс WAVE.


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



Чтобы воспроизвести ресурс-волна с помощью этой функции, передайте в функцию указатель на строку, содержащую имя ресурса, как показано в следующем примере.


```C++
PlayResource("soundName"); 
```



 

 
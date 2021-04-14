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
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487696"
---
# <a name="playing-wave-resources"></a><span data-ttu-id="d2cec-109">Воспроизведение ЗВУКовых ресурсов</span><span class="sxs-lookup"><span data-stu-id="d2cec-109">Playing WAVE Resources</span></span>

<span data-ttu-id="d2cec-110">Функцию [**PlaySound**](/previous-versions//dd743680(v=vs.85)) можно использовать для воспроизведения звука, хранящегося в виде ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2cec-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="d2cec-111">Хотя это и возможно с помощью функции [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) , **сндплайсаунд** требует поиска, загрузки, блокировки, разблокировки и освобождения ресурса. **PlaySound** все это достигается с помощью одной строки кода.</span><span class="sxs-lookup"><span data-stu-id="d2cec-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="d2cec-112">Пример PlaySound</span><span class="sxs-lookup"><span data-stu-id="d2cec-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="d2cec-113">Пример Сндплайсаунд</span><span class="sxs-lookup"><span data-stu-id="d2cec-113">sndPlaySound Example</span></span>

<span data-ttu-id="d2cec-114">\_Флаг памяти snd указывает, что параметр *лпсзсаунднаме* является указателем на изображение файла Wave в памяти.</span><span class="sxs-lookup"><span data-stu-id="d2cec-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="d2cec-115">Чтобы включить файл WAVE в качестве ресурса в приложение, добавьте следующую запись в скрипт ресурсов приложения (. RC).</span><span class="sxs-lookup"><span data-stu-id="d2cec-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="d2cec-116">Имя *саунднаме* — это заполнитель для имени, которое указывается для ссылки на этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="d2cec-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="d2cec-117">ЗВУКовые ресурсы загружаются и доступны так же, как и другие ресурсы Windows, определяемые приложением.</span><span class="sxs-lookup"><span data-stu-id="d2cec-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="d2cec-118">Функция Плайресаурце в следующем примере воспроизводит указанный ресурс WAVE.</span><span class="sxs-lookup"><span data-stu-id="d2cec-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


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



<span data-ttu-id="d2cec-119">Чтобы воспроизвести ресурс-волна с помощью этой функции, передайте в функцию указатель на строку, содержащую имя ресурса, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d2cec-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 
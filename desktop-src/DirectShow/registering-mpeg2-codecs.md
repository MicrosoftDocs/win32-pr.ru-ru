---
description: Регистрация кодеков MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Регистрация кодеков MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139742"
---
# <a name="registering-mpeg2-codecs"></a><span data-ttu-id="1190f-103">Регистрация кодеков MPEG2</span><span class="sxs-lookup"><span data-stu-id="1190f-103">Registering MPEG2 Codecs</span></span>

<span data-ttu-id="1190f-104">Этот раздел относится только к Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="1190f-104">This topic applies to Windows XP Media Center Edition only.</span></span>

<span data-ttu-id="1190f-105">Windows XP Media Center Edition поддерживает два раздела реестра, которые используются для определения того, какой кодек используется для воспроизведения видео и звуковых файлов MPEG2.</span><span class="sxs-lookup"><span data-stu-id="1190f-105">Windows XP Media Center Edition maintains two registry keys that it uses to determine which codec to use to play back MPEG2 video and audio files.</span></span> <span data-ttu-id="1190f-106">Первый раздел реестра указывает предпочитаемый изготовителем компьютера кодек MPEG2, а второй — все кодеки, совместимые с Media Center, которые уже установлены на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1190f-106">The first registry key specifies the computer manufacturer's preferred MPEG2 codec, and the second lists all of the Media Center compatible codecs that are currently installed on the computer.</span></span> <span data-ttu-id="1190f-107">Когда Media Center должен воспроизвести файл MPEG2, он использует предпочтительный кодек производителя, если он указан.</span><span class="sxs-lookup"><span data-stu-id="1190f-107">When Media Center needs to play back an MPEG2 file, it uses the manufacturer's preferred codec, if one is specified.</span></span> <span data-ttu-id="1190f-108">В противном случае используется первый совместимый с Media Center кодек, указанный в реестре.</span><span class="sxs-lookup"><span data-stu-id="1190f-108">If not, it uses the first Media Center compatible codec listed in the registry.</span></span> <span data-ttu-id="1190f-109">Если в реестре нет предпочтительных или совместимых кодеков, Media Center использует стандартный фильтр DirectShow для выбора кодека.</span><span class="sxs-lookup"><span data-stu-id="1190f-109">If the registry specifies no preferred or compatible codecs, Media Center uses the standard DirectShow filter merit to choose a codec.</span></span>

<span data-ttu-id="1190f-110">Чтобы гарантировать, что Media Center всегда использует совместимый кодек MPEG2, производители компьютеров Media Center должны указать предпочтительный кодек MPEG2 в следующем расположении реестра:</span><span class="sxs-lookup"><span data-stu-id="1190f-110">To ensure that Media Center always uses a compatible MPEG2 codec, manufacturers of Media Center computers should specify the preferred MPEG2 codec at the following registry location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



<span data-ttu-id="1190f-111">Ключевые данные должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1190f-111">The key data should be as follows:</span></span>


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



<span data-ttu-id="1190f-112">Программа установки для совместимого с Media Center кодека MPEG2 должна зарегистрировать кодек, создав два экземпляра следующего раздела реестра — один для видеокодека и один для аудиокодека:</span><span class="sxs-lookup"><span data-stu-id="1190f-112">The setup program for a Media Center compatible MPEG2 codec should register the codec by creating two instances of the following registry key—one for the video codec and one for the audio codec:</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



<span data-ttu-id="1190f-113">Ключевые данные должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1190f-113">The key data should be as follows:</span></span>


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 




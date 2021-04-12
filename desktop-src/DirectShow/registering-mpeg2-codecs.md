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
# <a name="registering-mpeg2-codecs"></a>Регистрация кодеков MPEG2

Этот раздел относится только к Windows XP Media Center Edition.

Windows XP Media Center Edition поддерживает два раздела реестра, которые используются для определения того, какой кодек используется для воспроизведения видео и звуковых файлов MPEG2. Первый раздел реестра указывает предпочитаемый изготовителем компьютера кодек MPEG2, а второй — все кодеки, совместимые с Media Center, которые уже установлены на компьютере. Когда Media Center должен воспроизвести файл MPEG2, он использует предпочтительный кодек производителя, если он указан. В противном случае используется первый совместимый с Media Center кодек, указанный в реестре. Если в реестре нет предпочтительных или совместимых кодеков, Media Center использует стандартный фильтр DirectShow для выбора кодека.

Чтобы гарантировать, что Media Center всегда использует совместимый кодек MPEG2, производители компьютеров Media Center должны указать предпочтительный кодек MPEG2 в следующем расположении реестра:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



Ключевые данные должны выглядеть следующим образом:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Программа установки для совместимого с Media Center кодека MPEG2 должна зарегистрировать кодек, создав два экземпляра следующего раздела реестра — один для видеокодека и один для аудиокодека:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



Ключевые данные должны выглядеть следующим образом:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 




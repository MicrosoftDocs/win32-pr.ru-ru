---
title: Поведение драйверов по умолчанию
description: Поведение драйверов по умолчанию
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791071"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="5c5de-103">Поведение драйверов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5c5de-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="5c5de-104">Во многих случаях спецификации команды MCI определяют значения по умолчанию и поведение для драйверов определенного типа устройства.</span><span class="sxs-lookup"><span data-stu-id="5c5de-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="5c5de-105">Так как мультимедийные устройства могут иметь широкий спектр функций (и ограничений), могут быть неопределенными областями поведения.</span><span class="sxs-lookup"><span data-stu-id="5c5de-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="5c5de-106">Кроме того, драйверы могут выполнять исключения по-разному в зависимости от возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="5c5de-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="5c5de-107">Например, рассмотрим следующие команды, отправляемые драйверу звуковой волны с помощью функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="5c5de-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="5c5de-108">Команда [**Record**](record.md) возвращает значение "параметр вне допустимого диапазона" и останавливает воспроизведение, запущенное предыдущей командой [**Play**](play.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5de-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="5c5de-109">Можно ожидать, что драйвер проверяет команду записи перед остановкой воспроизведения, но драйвер останавливает воспроизведение первыми.</span><span class="sxs-lookup"><span data-stu-id="5c5de-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 
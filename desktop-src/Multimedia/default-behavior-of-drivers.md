---
title: Поведение драйверов по умолчанию
description: Поведение драйверов по умолчанию
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61312010759ddd1bf152f0e51f7605bda1954329096913b61dac14a671908f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144527"
---
# <a name="default-behavior-of-drivers"></a>Поведение драйверов по умолчанию

Во многих случаях спецификации команды MCI определяют значения по умолчанию и поведение для драйверов определенного типа устройства. Так как мультимедийные устройства могут иметь широкий спектр функций (и ограничений), могут быть неопределенными областями поведения. Кроме того, драйверы могут выполнять исключения по-разному в зависимости от возможностей устройства.

Например, рассмотрим следующие команды, отправляемые драйверу звуковой волны с помощью функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Команда [**Record**](record.md) возвращает значение "параметр вне допустимого диапазона" и останавливает воспроизведение, запущенное предыдущей командой [**Play**](play.md) . Можно ожидать, что драйвер проверяет команду записи перед остановкой воспроизведения, но драйвер останавливает воспроизведение первыми.

 

 
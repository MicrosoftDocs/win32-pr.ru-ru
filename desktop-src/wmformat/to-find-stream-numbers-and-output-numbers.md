---
title: Поиск номеров потоков и выходных номеров
description: Поиск номеров потоков и выходных номеров
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Расширенный системный формат (ASF), Номера потоков
- ASF (Расширенный системный формат), создание чисел
- Расширенный формат систем (ASF), Поиск выходных номеров
- ASF (Расширенный системный формат), Поиск выходных номеров
- синхронные читатели, Номера потоков
- синхронные читатели, Поиск выходных номеров
- потоки, Поиск чисел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788737"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Поиск номеров потоков и выходных номеров

Синхронный модуль чтения поддерживает более упрощенное переключение между потоком и выходными номерами для воспроизведения, чем асинхронный модуль чтения. Поэтому важно иметь возможность определить, какие номера потоков эквивалентны выходным номерам или наоборот.

Чтобы найти номер выхода, соответствующий номеру потока, вызовите метод [**ивмсинкреадер:: жетаутпутнумберфорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Чтобы найти номер потока, соответствующий выходному номеру, вызовите метод [ **ивмсинкреадер:: жетстреамнумберфораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Входы, потоки и выходные данные**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699592"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Поиск номеров потоков и выходных номеров

Синхронный модуль чтения поддерживает более упрощенное переключение между потоком и выходными номерами для воспроизведения, чем асинхронный модуль чтения. Поэтому важно иметь возможность определить, какие номера потоков эквивалентны выходным номерам или наоборот.

Чтобы найти номер выхода, соответствующий номеру потока, вызовите метод [**ивмсинкреадер:: жетаутпутнумберфорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Чтобы найти номер потока, соответствующий выходному номеру, вызовите метод [ **ивмсинкреадер:: жетстреамнумберфораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**входные данные, Потоки и выходные данные**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





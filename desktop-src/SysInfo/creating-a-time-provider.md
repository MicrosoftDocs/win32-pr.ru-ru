---
description: Поставщик времени реализуется в виде библиотеки DLL. Каждая библиотека DLL может поддерживать несколько поставщиков времени. Каждый поставщик отвечает за собственную конфигурацию и синхронизацию.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Создание поставщика времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58766bf0ed7339bf8c9bfd7abc7434ddc43165b7cbdd77bcfd5420947e743d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885767"
---
# <a name="creating-a-time-provider"></a>Создание поставщика времени

Поставщик времени реализуется в виде библиотеки DLL. Каждая библиотека DLL может поддерживать несколько поставщиков времени. Каждый поставщик отвечает за собственную конфигурацию и синхронизацию.

Поставщики времени должны реализовывать следующие функции обратного вызова:

-   [**тимепровклосе**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**тимепровкомманд**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**тимепровопен**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

После загрузки библиотеки DLL поставщика Диспетчер поставщиков времени вызывает [**тимепровопен**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), передавая имя поставщика и указатели на следующие функции:

-   [**алертсамплесаваилфунк**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**жеттимесисинфофунк**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**логтимепровевентфунк**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Эти функции предназначены для использования поставщиком времени. Поставщик времени использует [**тимепровопен**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) для возврата маркера поставщика, используемого диспетчером поставщиков времени при отправке команд поставщику времени. Значение Handle определяется поставщиком времени и используется в основном для различения разных поставщиков, реализованных в одной и той же библиотеке DLL. Поставщик времени может регистрировать важные события с помощью [**логтимепровевентфунк**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).

Диспетчер поставщиков времени использует [**тимепровкомманд**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) для отправки команд поставщику времени. Когда поставщику времени необходимо уведомить Диспетчер поставщиков времени о наличии доступных образцов времени, он вызывает [**алертсамплесаваилфунк**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc). Затем Диспетчер поставщиков времени вызывает **тимепровкомманд** с помощью команды TPC \_ ресамплинг для получения образцов времени. Для запроса образца диспетчером поставщиков времени может потребоваться до 16 секунд. Поэтому приложение не должно ждать запроса.

Чтобы обеспечить точность, поставщик времени должен получить все сведения, связанные со временем, с помощью [**жеттимесисинфофунк**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).

Когда время завершения работы поставщика времени завершается, Диспетчер поставщиков времени вызывает [**тимепровклосе**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 




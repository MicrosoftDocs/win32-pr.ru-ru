---
title: Использование записи для просмотра
description: Использование записи для просмотра
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Расширенный формат систем (ASF), просмотр записи
- ASF (Расширенный системный формат), пишущий Просмотр
- Расширенный формат систем (ASF), просмотр
- ASF (Расширенный системный формат), просмотр
- Просмотр для записи
- Просмотр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533053"
---
# <a name="to-use-writer-postview"></a>Использование записи для просмотра

Объект модуля записи предоставляет возможности просмотра, что позволяет проверять написание содержимого без необходимости настройки объекта модуля чтения. Объект модуля записи не поддерживает просмотр аудио содержимого.

Модуль записи Writer работает во многом так же, как и асинхронный объект Reader, с меньшим числом функций. Подробные сведения о чтении цифровых носителей см. в разделе [чтение файлов ASF](reading-asf-files.md).

Чтобы реализовать средство просмотра, выполните следующие действия.

1.  Реализуйте обратный вызов [**ивмвритерпоствиевкаллбакк:: онпоствиевсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) . Этот метод, по сути, аналогичен [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , за исключением того, что он указывает номера потоков вместо выходных данных.
2.  Настройка для записи в обычном режиме.
3.  Получите указатель на интерфейс [**ивмвритерпоствиев**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) объекта Writer, вызвав **Ивмвритер:: QueryInterface**.
4.  Задайте обратный вызов для проверяющего для использования с помощью вызова [**ивмвритерпоствиев:: сетпоствиевкаллбакк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Для каждого потока, для которого необходимо получить образцы просмотра, вызовите метод [**ивмвритерпоствиев:: сетрецеивепоствиевсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Можно проверить, настроен ли поток на получение образцов просмотра с помощью вызова [**ивмвритерпоствиев:: жетрецеивепоствиевсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  Вы можете манипулировать образцами форматов, как в случае с выходными форматами в объекте Reader или синхронном объекте Reader.
7.  Когда вы начинаете писать файл, вы начнете получать примеры в реализации метода обратного вызова **онпоствиевсампле** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмвритерпоствиевкаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 





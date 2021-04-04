---
title: Получение статистики модуля записи
description: Получение статистики модуля записи
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Расширенный системный формат (ASF), статистика записи
- ASF (Расширенный системный формат), статистика записи
- Статистика модуля записи, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103987274"
---
# <a name="to-get-writer-statistics"></a>Получение статистики модуля записи

Модуль записи может предоставлять статистические сведения о операциях записи. Существует два метода для сбора статистики модуля записи: [**ивмвритерадванцед::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) IWMWriterAdvanced3 и [**:: жетстатистиксекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Сведения, полученные с помощью **жетстатистиксекс** , являются более точными, чем сведения, полученные функцией **статистики**.

Оба метода заполняют структуры статистическими данными. **В статистике** используется [**Структура \_ \_ статистики модуля записи WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) , а в **жетстатистиксекс** используется структура [**\_ \_ Statistics \_ модуля записи WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) . **Жетстатистиксекс** не дублирует данные, полученные функцией **статистики**. Для получения наиболее полных сведений следует вызывать оба метода.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмвритерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Интерфейс IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 





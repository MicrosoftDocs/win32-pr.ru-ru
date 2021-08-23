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
ms.openlocfilehash: a1cedd96f1e94b8d3c9499fe08e3eeebb2100e866b141b756483cfb07bb7cb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083969"
---
# <a name="to-get-writer-statistics"></a>Получение статистики модуля записи

Модуль записи может предоставлять статистические сведения о операциях записи. Существует два метода для сбора статистики модуля записи: [**ивмвритерадванцед::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) IWMWriterAdvanced3 и [**:: жетстатистиксекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Сведения, полученные с помощью **жетстатистиксекс** , являются более точными, чем сведения, полученные функцией **статистики**.

Оба метода заполняют структуры статистическими данными. **В статистике** используется [**Структура \_ \_ статистики модуля записи WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) , а в **жетстатистиксекс** используется структура [**\_ \_ Statistics \_ модуля записи WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) . **Жетстатистиксекс** не дублирует данные, полученные функцией **статистики**. Для получения наиболее полных сведений следует вызывать оба метода.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмвритерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Интерфейс IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 





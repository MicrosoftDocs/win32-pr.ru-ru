---
title: Рекомендации по WinRM
description: В этом разделе объясняются некоторые рекомендации по использованию различных функций API WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733804"
---
# <a name="winrm-best-practices"></a>Рекомендации по WinRM

В этом разделе объясняются некоторые рекомендации по использованию различных функций API WinRM.

## <a name="quotas"></a>Квоты

При достижении квоты служба WinRM возвращает клиенту сообщение об ошибке. В результате клиентская логика должна явным образом повторить операцию на основе возвращенной ошибки.

## <a name="event-subscriptions"></a>Подписки на события

при использовании подписок, инициированных сборщиком, ограничьте число удаленных компьютеров до 500 и изолируйте [Windows службу сборщика событий](/windows/desktop/WEC/windows-event-collector) (вексвк) в отдельном хост-процессе.

Ошибка подключения будет содержать поток до истечения времени ожидания. Большое количество одновременных ошибок подключения может привести к нехватке пула потоков и отрисовывать сервер без ответа.

 

 
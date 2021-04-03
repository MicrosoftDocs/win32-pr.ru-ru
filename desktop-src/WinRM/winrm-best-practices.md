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
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987562"
---
# <a name="winrm-best-practices"></a>Рекомендации по WinRM

В этом разделе объясняются некоторые рекомендации по использованию различных функций API WinRM.

## <a name="quotas"></a>Квоты

При достижении квоты служба WinRM возвращает клиенту сообщение об ошибке. В результате клиентская логика должна явным образом повторить операцию на основе возвращенной ошибки.

## <a name="event-subscriptions"></a>Подписки на события

При использовании подписок, инициированных сборщиком, ограничьте число удаленных компьютеров до 500 и изолируйте службу [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) (вексвк) в отдельном хост-процессе.

Ошибка подключения будет содержать поток до истечения времени ожидания. Большое количество одновременных ошибок подключения может привести к нехватке пула потоков и отрисовывать сервер без ответа.

 

 
---
title: Завершение задания и его отмена
description: Чтобы завершить задание перемещения, вызовите метод использованием метода ibackgroundcopyjob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- передачи битов задания, отмена
- Отмена битов задания
- БИТЫ заданий передачи, завершение
- завершение битов задания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486652"
---
# <a name="completing-and-canceling-a-job"></a>Завершение задания и его отмена

Чтобы завершить задание перемещения, вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Для заданий загрузки можно вызвать метод **Complete** до передачи всех файлов в задании (до того, как состояние задания передано в состояние задания BG \_ \_ \_ ). Пользователю будут доступны только те файлы, которые были успешно переданы клиенту службой BITS до вызова метода **Complete** .

Для заданий отправки вызовите метод [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) только в том случае, если состояние задания — \_ « \_ Передача состояния задания BG» \_ . Чтобы определить, когда состояние задания — \_ \_ передано состояние задания BG \_ , следует [опросить](polling-for-the-status-of-the-job.md) свойство состояния задания или зарегистрировать, чтобы получить \_ уведомление о \_ \_ [событии](registering-a-com-callback.md)переданного задания в BG.

Чтобы отменить задание на перемещение, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . Метод **Cancel** удаляет задание из очереди на перемещение и удаляет временные файлы с клиента. Как правило, этот метод вызывается, если не удается разрешить ошибку, связанную с заданием.

Метод [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) отменяет отправку, если передача не завершена. Если передача завершена, а задание имеет тип \_ задания BG \_ \_ upload \_ , метод отменяет ответ.

Если не вызвать метод [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) или метод [**использованием метода ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) в течение 90 дней (по умолчанию [жобинактивититимеаут](group-policies.md) групповая политика), служба отменяет задание. Если служба отменяет задание, скачанные файлы и файл ответов недоступны для клиента. Отмена заданий не влияет на успешно отправленные файлы. Следует всегда вызывать метод **Complete** или **Cancel** и не полагаться на политику жобинактивититимеаут для очистки заданий. Задания, оставшиеся в очереди, могут помешать пользователям создавать другие задания при достижении предела политики Maxjobspermachine или MaxJobsPerMachine.

 

 





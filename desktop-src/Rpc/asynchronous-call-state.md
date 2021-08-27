---
title: Асинхронное состояние вызова
description: На этой странице описывается асинхронное состояние вызова для вызовов RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478630"
---
# <a name="asynchronous-call-state"></a>Асинхронное состояние вызова

На этой странице описывается асинхронное состояние вызова для вызовов RPC.

## <a name="client-behavior"></a>Поведение клиента




| Состояние | Имя состояния | Действие | 
|-------|------------|--------|
| C | Сделать вызов | Создание RPC<ul><li>При успешном завершении переходит в состояние Вкомп</li><li>При возникновении исключения перейдите в конец</li></ul>Сбой: перейдите на страницу Can<br /> | 
| Можно | Отменить вызов | Вызов <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>рпкасинкканцелкалл</strong></a>Go to вкомп<br /> | 
| вкомп | Ожидание завершения | Ожидается получение уведомления Нотификатионкалл-Complete<br /> К Comp<br /> | 
| Соответствовал | Completion | Выдача <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>рпкасинккомплетекалл</strong></a>к концу<br /> | 
| Конец | 




 

## <a name="server-behavior"></a>Поведение сервера



| Состояние | Имя состояния     | Действие                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | Вызов отправляется RPC Рунтимепроцесс<br/> К Comp<br/> Неустранимая ошибка (при выполнении в потоке RPC): вызов исключения; к концу<br/> Для корректного сбоя: перейдите на<br/> |
| А     | Прервать вызов | Вызов [**рпкасинкаборткалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)к концу<br/>                                                                                                                                             |
| Соответствовал  | Completion     | Выдача [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)к концу<br/>                                                                                                                                      |
| Конец   |                |                                                                                                                                                                                                                     |



 

 

 






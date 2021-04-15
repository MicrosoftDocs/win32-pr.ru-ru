---
description: 'Дополнительные сведения: вопросы программирования при написании диспетчеров ресурсов'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Вопросы программирования при написании диспетчеров ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683609"
---
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="1129d-103">Вопросы программирования при написании диспетчеров ресурсов</span><span class="sxs-lookup"><span data-stu-id="1129d-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="1129d-104">При использовании API диспетчера транзакций ядра для добавления поддержки транзакций в приложения учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="1129d-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="1129d-105">При написании собственного диспетчера ресурсов у вас должны быть хорошие и работающие знания методик и протоколов управления транзакциями.</span><span class="sxs-lookup"><span data-stu-id="1129d-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="1129d-106">Если вы не записываете диспетчеры ресурсов должным образом, вы можете повредить собственные данные при неправильной обработке операций восстановления.</span><span class="sxs-lookup"><span data-stu-id="1129d-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="1129d-107">Можно также закрепить заключительный фрагмент журнала транзакций и заполнить файловую систему журналами транзакций.</span><span class="sxs-lookup"><span data-stu-id="1129d-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="1129d-108">Если политика размера журнала не запрещает увеличение размера журнала, то диспетчер ресурсов не будет прекращать выполнение транзакций.</span><span class="sxs-lookup"><span data-stu-id="1129d-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="1129d-109">Диспетчер ресурсов должен прерывать обновление системы, чтобы не перерасходовать ресурсы файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1129d-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="1129d-110">Для управления доступом к файлам журнала диспетчеры ресурсов должны использовать списки управления доступом (ACL). в противном случае атаки типа "отказ в обслуживании" возможны.</span><span class="sxs-lookup"><span data-stu-id="1129d-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="1129d-111">Любой диспетчер ресурсов или участник транзакций, который кэширует данные, должен быть прикреплен к предварительно подготовленным уведомлениям.</span><span class="sxs-lookup"><span data-stu-id="1129d-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="1129d-112">При получении уведомления о предварительной подготовке необходимо сбросить все данные, чтобы все нисходящие диспетчеры ресурсов могли прикрепляться перед фазой подготовки.</span><span class="sxs-lookup"><span data-stu-id="1129d-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="1129d-113">Дальнейшая работа в этой транзакции не должна кэшироваться.</span><span class="sxs-lookup"><span data-stu-id="1129d-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="1129d-114">Не закрывайте обработчик прикрепления, пока транзакция все еще активна; Это приведет к откату транзакции.</span><span class="sxs-lookup"><span data-stu-id="1129d-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 




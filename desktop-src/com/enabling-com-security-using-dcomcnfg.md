---
title: Включение безопасности COM с помощью DCOMCNFG
description: Программа Dcomcnfg.exe предоставляет пользовательский интерфейс для изменения определенных параметров в реестре.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691168"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="993e2-103">Включение безопасности COM с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="993e2-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="993e2-104">Программа Dcomcnfg.exe предоставляет пользовательский интерфейс для изменения определенных параметров в реестре.</span><span class="sxs-lookup"><span data-stu-id="993e2-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="993e2-105">С помощью Dcomcnfg.exe можно включить безопасность как на уровне компьютера, так и на уровне всего процесса.</span><span class="sxs-lookup"><span data-stu-id="993e2-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="993e2-106">Можно включить безопасность для конкретного компьютера, чтобы в случае, когда процесс не предоставит собственные параметры безопасности либо программно, либо через значения реестра, будут использоваться значения, заданные Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="993e2-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="993e2-107">Также можно использовать Dcomcnfg.exe, чтобы включить безопасность только для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="993e2-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="993e2-108">При включении безопасности необходимо выполнить две основные задачи:</span><span class="sxs-lookup"><span data-stu-id="993e2-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="993e2-109">Установите уровень проверки подлинности, отличный от None.</span><span class="sxs-lookup"><span data-stu-id="993e2-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="993e2-110">Задайте разрешения, включая разрешения на запуск и на доступ.</span><span class="sxs-lookup"><span data-stu-id="993e2-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="993e2-111">Действия, выполняемые для выполнения этих задач, зависят от того, включена ли безопасность для всего компьютера или только для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="993e2-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="993e2-112">Кроме того, может потребоваться задать другие значения для компьютера или приложения.</span><span class="sxs-lookup"><span data-stu-id="993e2-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="993e2-113">Для запуска Dcomcnfg.exe требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="993e2-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="993e2-114">В следующих разделах приводятся пошаговые инструкции по настройке безопасности с помощью Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="993e2-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="993e2-115">Настройка безопасности System-Wide с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="993e2-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="993e2-116">Настройка безопасности Процессвиде с помощью DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="993e2-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="993e2-117">См. также</span><span class="sxs-lookup"><span data-stu-id="993e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="993e2-118">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="993e2-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="993e2-119">Отключение безопасности</span><span class="sxs-lookup"><span data-stu-id="993e2-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 





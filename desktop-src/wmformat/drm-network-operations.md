---
title: Сетевые операции DRM
description: Сетевые операции DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK, сетевые операции DRM
- Расширенный формат систем (ASF), сетевые операции DRM
- ASF (Расширенный системный формат), сетевые операции DRM
- Управление цифровыми правами (DRM), сетевые операции
- DRM (Управление цифровыми правами), сетевые операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328691"
---
# <a name="drm-network-operations"></a><span data-ttu-id="6ca7f-108">Сетевые операции DRM</span><span class="sxs-lookup"><span data-stu-id="6ca7f-108">DRM Network Operations</span></span>

<span data-ttu-id="6ca7f-109">Для нескольких операций, связанных с DRM, приложению требуется подключение к службе, работающей в сети.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="6ca7f-110">Эти операции включают в себя индивидуальные действия, получение лицензий, отзыв лицензий, а затем резервное копирование и восстановление лицензий.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="6ca7f-111">Как и в случае с любой сетевой транзакцией, приложение должно учитывать различные проблемы при включении функций, требующих сетевых операций.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="6ca7f-112">Приложение должно отвести себя от состояния операции к любому экстенту, который может использоваться для конкретной функции, обычно посредством обработки сообщений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="6ca7f-113">Вы должны предоставить отзыв пользователю о состоянии.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="6ca7f-114">Если при первой попытке выполнить операцию не удается, пользователю следует предоставить возможность повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="6ca7f-115">Во многих случаях первая попытка сталкивается с трудностями, но последующая попытка завершается без ошибок.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="6ca7f-116">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="6ca7f-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6ca7f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6ca7f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ca7f-118">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="6ca7f-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 





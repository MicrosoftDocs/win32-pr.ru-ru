---
title: Локальное хранилище лицензий
description: Локальное хранилище лицензий
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, лицензии DRM
- Пакет SDK для Windows Media Format, лицензии для DRM
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), лицензирование защищенных файлов
- DRM (Управление цифровыми правами), лицензирование защищенных файлов
- лицензии, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411380"
---
# <a name="local-license-store"></a><span data-ttu-id="2cc46-111">Локальное хранилище лицензий</span><span class="sxs-lookup"><span data-stu-id="2cc46-111">Local License Store</span></span>

<span data-ttu-id="2cc46-112">При доставке лицензии DRM на клиентский компьютер она помещается в локальное хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="2cc46-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="2cc46-113">Это защищенный файл на жестком диске, содержащий все лицензии, выданные пользователю вместе с другими данными DRM.</span><span class="sxs-lookup"><span data-stu-id="2cc46-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="2cc46-114">Вы можете управлять данными в локальном хранилище лицензий несколькими ограниченными способами с помощью расширенных API-интерфейсов клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2cc46-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="2cc46-115">Помимо локального хранилища лицензий, некоторые объекты используют временное хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="2cc46-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="2cc46-116">Лицензия во временном хранилище существует только в течение короткого периода времени.</span><span class="sxs-lookup"><span data-stu-id="2cc46-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="2cc46-117">Однако некоторые лицензии, которые начинаются во временном хранилище, можно сохранить в обычном локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="2cc46-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cc46-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2cc46-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cc46-119">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="2cc46-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 





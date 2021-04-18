---
title: Эксклюзивные Интернет-магазины
description: Эксклюзивные Интернет-магазины
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Интернет-магазины проигрывателя Windows Media, монопольные
- Интернет-магазины, монопольные
- Тип 1 Интернет-магазины, монопольно
- Тип 2 Интернет-магазинов, монопольно
- Эксклюзивные Интернет-магазины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691438"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="8db82-108">Эксклюзивные Интернет-магазины</span><span class="sxs-lookup"><span data-stu-id="8db82-108">Exclusive Online Stores</span></span>

<span data-ttu-id="8db82-109">В проигрывателе Windows Media 11 приложение, которое внедряет удаленное управление проигрывателем, может указывать эксклюзивное Интернет-хранилище.</span><span class="sxs-lookup"><span data-stu-id="8db82-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="8db82-110">В этом случае селектор службы в проигрывателе Windows Media отключается, и пользователю доступно только указанное Интернет-хранилище.</span><span class="sxs-lookup"><span data-stu-id="8db82-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="8db82-111">Кроме того, проигрыватель Windows Media принимает цвет, указанный в элементе **Color** serviceInfo документа Online Store.</span><span class="sxs-lookup"><span data-stu-id="8db82-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="8db82-112">Чтобы указать эксклюзивное Интернет-хранилище, приложение должно добавить Ексклусивесервице:*keyName* в конец строки, возвращаемой из [Ивмпремотемедиасервицес:: жетсервицетипе](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span><span class="sxs-lookup"><span data-stu-id="8db82-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="8db82-113">Например, предположим, что Proseware — это имя ключа, присвоенное конкретному сетевому магазину.</span><span class="sxs-lookup"><span data-stu-id="8db82-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="8db82-114">Если **жетсервицетипе** возвращает строку "Remote Ексклусивесервице: Proseware", то Proseware будет единственным интернет-хранилищем, доступным в удаленном элементе управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="8db82-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="8db82-115">Приложение может ограничить проигрыватель Windows Media эксклюзивным Интернет-хранилищем только в том случае, если проигрыватель Windows Media еще не запущен при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="8db82-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="8db82-116">Ответственность за то, чтобы сообщить пользователю о необходимости закрыть проигрыватель Windows Media перед запуском приложения, является обязанностью приложения.</span><span class="sxs-lookup"><span data-stu-id="8db82-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db82-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8db82-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db82-118">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="8db82-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8db82-119">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8db82-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





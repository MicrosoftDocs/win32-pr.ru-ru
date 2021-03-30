---
title: Частные Интернет-магазины
description: Частные Интернет-магазины
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Интернет-магазины проигрывателя Windows Media, частные
- Интернет-магазины, частные
- Тип 1 Интернет-магазины, частный
- Тип 2 онлайн-магазина, частный
- частные Интернет-магазины
- реестр, частные Интернет-магазины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411137"
---
# <a name="private-online-stores"></a><span data-ttu-id="cff87-109">Частные Интернет-магазины</span><span class="sxs-lookup"><span data-stu-id="cff87-109">Private Online Stores</span></span>

<span data-ttu-id="cff87-110">Проигрыватель Windows Media 10 или более поздней версии поддерживает частные Интернет-магазины; Это значит, что хранилища видны только определенным пользователям.</span><span class="sxs-lookup"><span data-stu-id="cff87-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="cff87-111">Чтобы частный Интернет-магазин отображался для текущего пользователя, необходимо иметь запись, представляющую частный Интернет-магазин в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="cff87-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="cff87-112">HKEY \_ текущее \_ пользовательское \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ приватесервицес</span><span class="sxs-lookup"><span data-stu-id="cff87-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="cff87-113">Требуемая запись реестра должна иметь следующий формат.</span><span class="sxs-lookup"><span data-stu-id="cff87-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="cff87-114">Имя</span><span class="sxs-lookup"><span data-stu-id="cff87-114">Name</span></span>                                                         | <span data-ttu-id="cff87-115">Тип</span><span class="sxs-lookup"><span data-stu-id="cff87-115">Type</span></span>           | <span data-ttu-id="cff87-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cff87-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="cff87-117">Любое имя, выбранное пользователем, который создает запись реестра</span><span class="sxs-lookup"><span data-stu-id="cff87-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="cff87-118">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cff87-118">**REG\_DWORD**</span></span> | <span data-ttu-id="cff87-119">Число, предоставляемое корпорацией Майкрософт, которое идентифицирует частный Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="cff87-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="cff87-120">Элемент управления ActiveX проигрывателя Windows Media 10 поддерживает частные Интернет-магазины только в том случае, если элемент управления работает в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="cff87-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="cff87-121">Элемент управления ActiveX проигрывателя Windows Media 11 поддерживает частные Интернет-магазины независимо от того, работает ли элемент управления в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="cff87-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cff87-122">См. также</span><span class="sxs-lookup"><span data-stu-id="cff87-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff87-123">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="cff87-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





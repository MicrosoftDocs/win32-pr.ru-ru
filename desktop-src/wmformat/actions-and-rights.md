---
title: Действия и права
description: Действия и права
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, лицензии DRM
- Пакет SDK для Windows Media Format, лицензии для DRM
- Управление цифровыми правами (DRM), действия
- DRM (Управление цифровыми правами), действия
- Управление цифровыми правами (DRM), права
- DRM (Управление цифровыми правами), права доступа
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- лицензии, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067442"
---
# <a name="actions-and-rights"></a><span data-ttu-id="8db8d-113">Действия и права</span><span class="sxs-lookup"><span data-stu-id="8db8d-113">Actions and Rights</span></span>

<span data-ttu-id="8db8d-114">Если файл защищен с помощью Windows Media DRM, его использование полностью ограничено.</span><span class="sxs-lookup"><span data-stu-id="8db8d-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="8db8d-115">Лицензии могут быть выпущены, чтобы пользователи могли использовать содержимое в конкретных целях.</span><span class="sxs-lookup"><span data-stu-id="8db8d-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="8db8d-116">Каждый способ, которым пользователь может использовать содержимое, описывается действием.</span><span class="sxs-lookup"><span data-stu-id="8db8d-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="8db8d-117">Например, действием является воспроизведение файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8db8d-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="8db8d-118">Считается, что лицензия, позволяющая заданное действие, предоставляет право.</span><span class="sxs-lookup"><span data-stu-id="8db8d-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="8db8d-119">Например, лицензия может предоставить право на воспроизведение содержимого на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8db8d-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="8db8d-120">Действия и права ссылаются на те же способы использования содержимого.</span><span class="sxs-lookup"><span data-stu-id="8db8d-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="8db8d-121">Разница заключается в том, что действие относится к использованию, а право указывает на разрешение.</span><span class="sxs-lookup"><span data-stu-id="8db8d-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="8db8d-122">Несмотря на это различие, слова Action и right часто взаимозаменяемы в этой документации и других документах, описывающих DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8db8d-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="8db8d-123">Действия, управляемые правами DRM в Windows Media, перечислены в разделе [константы прав](rights-constants.md) этой документации.</span><span class="sxs-lookup"><span data-stu-id="8db8d-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="8db8d-124">Некоторые методы расширенных API клиента DRM Windows Media используют разные константы для ссылки на базовые права DRM.</span><span class="sxs-lookup"><span data-stu-id="8db8d-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="8db8d-125">Например, метод [**ивмдрмлиценсекуери:: куерилиценсестате**](iwmdrmlicensequery-querylicensestate.md) использует набор строк, характерных для состояний лицензии.</span><span class="sxs-lookup"><span data-stu-id="8db8d-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="8db8d-126">Хотя эти константы определяют разные строки, чем базовые константы прав, они ссылаются на те же права в лицензии.</span><span class="sxs-lookup"><span data-stu-id="8db8d-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db8d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8db8d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db8d-128">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="8db8d-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 





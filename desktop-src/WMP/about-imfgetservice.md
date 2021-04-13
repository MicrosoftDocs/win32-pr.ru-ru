---
title: О Имфжетсервице
description: О Имфжетсервице
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Подключаемые модули проигрывателя Windows Media, интерфейсы
- подключаемые модули, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейсы
- Подключаемые модули DSP, интерфейсы
- интерфейсы, подключаемые модули DSP
- Подключаемые модули проигрывателя Windows Media, интерфейс Имфжетсервице
- подключаемые модули, интерфейс Имфжетсервице
- подключаемые модули обработки цифровых сигналов, интерфейс Имфжетсервице
- Подключаемые модули DSP, интерфейс Имфжетсервице
- Интерфейс Имфжетсервице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328667"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="71a02-113">О Имфжетсервице</span><span class="sxs-lookup"><span data-stu-id="71a02-113">About IMFGetService</span></span>

<span data-ttu-id="71a02-114">Интерфейс **имфжетсервице** — это один из интерфейсов, который должен быть реализован подключаемым модулем DSP с двойным режимом.</span><span class="sxs-lookup"><span data-stu-id="71a02-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="71a02-115">У него есть только один метод, **услуга**.</span><span class="sxs-lookup"><span data-stu-id="71a02-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="71a02-116">Подключаемый модуль DSP реализует метод **WebService** , чтобы клиенты могли получать указатели на интерфейсы, поддерживаемые подключаемым модулем, когда подключаемый модуль выполняется в конвейере Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="71a02-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 





---
title: Возможная утечка D1104
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Фабрика была выпущена, но созданный из нее интерфейс все еще активен. Хотя после выпуска фабрики можно освободить ресурсы, это условие может указывать на утечку памяти.
keywords:
- D1104 возможная утечка Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333555"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="96a83-105">D1104: возможная утечка</span><span class="sxs-lookup"><span data-stu-id="96a83-105">D1104: Possible Leak</span></span>

<span data-ttu-id="96a83-106">\[ *Фабрика* фабрики \] была выпущена, но интерфейс интерфейса, \[  \] созданный на ее основе, все еще активен.</span><span class="sxs-lookup"><span data-stu-id="96a83-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="96a83-107">Хотя после выпуска фабрики можно освободить ресурсы, это условие может указывать на утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="96a83-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="96a83-108">Заполнители</span><span class="sxs-lookup"><span data-stu-id="96a83-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="96a83-109"><span id="factory"></span><span id="FACTORY"></span>*установлен*</span><span class="sxs-lookup"><span data-stu-id="96a83-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="96a83-110">Адрес выпущенной фабрики.</span><span class="sxs-lookup"><span data-stu-id="96a83-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="96a83-111"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="96a83-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="96a83-112">Адрес интерфейса, созданного на *фабрике*.</span><span class="sxs-lookup"><span data-stu-id="96a83-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="96a83-113">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="96a83-113">Error Level</span></span> | <span data-ttu-id="96a83-114">Сведения</span><span class="sxs-lookup"><span data-stu-id="96a83-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="96a83-115">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="96a83-115">Possible Causes</span></span>

<span data-ttu-id="96a83-116">Фабрика была выпущена, но созданный из нее интерфейс все еще активен.</span><span class="sxs-lookup"><span data-stu-id="96a83-116">The factory was released but the interface created from it is still alive.</span></span>

 

 





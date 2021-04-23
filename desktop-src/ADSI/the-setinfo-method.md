---
title: Метод Сетинфо
description: Метод IADs Сетинфо сохраняет текущие значения свойств этого объекта Active Directory из кэша свойств в базовом хранилище каталога. Это аналогично сбросу буфера на диск.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- Сетинфо ADSI, использование
- свойства ADSI, сохранение текущих значений свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328347"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="5c433-106">Метод Сетинфо</span><span class="sxs-lookup"><span data-stu-id="5c433-106">The SetInfo Method</span></span>

<span data-ttu-id="5c433-107">Метод [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) сохраняет текущие значения свойств этого объекта Active Directory из кэша свойств в базовом хранилище каталога.</span><span class="sxs-lookup"><span data-stu-id="5c433-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="5c433-108">Это аналогично сбросу буфера на диск.</span><span class="sxs-lookup"><span data-stu-id="5c433-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="5c433-109">[**Сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) обновляет объекты, уже существующие в каталоге, или создает новую запись каталога для вновь созданных объектов.</span><span class="sxs-lookup"><span data-stu-id="5c433-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="5c433-110">В момент вызова [**сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , если какие-либо значения кэша свойств были записаны с помощью управляющего кода [**путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) (например, свойство \_ AD \_ Update или свойства ADS), то \_ \_ соответствующие запросы передаются в базовую службу каталогов.</span><span class="sxs-lookup"><span data-stu-id="5c433-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 





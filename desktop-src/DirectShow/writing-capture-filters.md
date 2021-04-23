---
description: Запись фильтров записи
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Запись фильтров записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683623"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="a747b-103">Запись фильтров записи</span><span class="sxs-lookup"><span data-stu-id="a747b-103">Writing Capture Filters</span></span>

<span data-ttu-id="a747b-104">Написание фильтра записи аудио или видео для DirectShow не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a747b-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="a747b-105">Вместо этого DirectShow обеспечивает автоматическую поддержку устройств видеозаписи аудио и видео, использование фильтров оболочки и [перечислителя системных устройств](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="a747b-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="a747b-106">Дополнительные сведения о реализации драйвера устройства см. в документации по комплекту драйверов для Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="a747b-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="a747b-107">Этот раздел предназначен только для разработчиков, которым необходимо захватывать какие-либо пользовательские данные с необычного аппаратного устройства.</span><span class="sxs-lookup"><span data-stu-id="a747b-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="a747b-108">В этом разделе содержатся следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="a747b-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="a747b-109">Требования к ПИН-коду для фильтров захвата</span><span class="sxs-lookup"><span data-stu-id="a747b-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="a747b-110">Реализация предварительной версии ПИН-кода (необязательно)</span><span class="sxs-lookup"><span data-stu-id="a747b-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="a747b-111">Создание данных в фильтре записи</span><span class="sxs-lookup"><span data-stu-id="a747b-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="a747b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a747b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a747b-113">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="a747b-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 




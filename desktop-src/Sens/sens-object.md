---
description: Служба уведомлений о системных событиях (Сенс) определяет кокласс Сенс как часть библиотеки типов Сенс.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Объект Сенс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664211"
---
# <a name="sens-object"></a><span data-ttu-id="798d3-103">Объект Сенс</span><span class="sxs-lookup"><span data-stu-id="798d3-103">SENS Object</span></span>

<span data-ttu-id="798d3-104">Служба уведомлений о системных событиях (Сенс) определяет кокласс Сенс как часть библиотеки типов Сенс.</span><span class="sxs-lookup"><span data-stu-id="798d3-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="798d3-105">Реализация</span><span class="sxs-lookup"><span data-stu-id="798d3-105">Implementation</span></span>

<span data-ttu-id="798d3-106">Реализация объекта Сенс обеспечивается операционной системой.</span><span class="sxs-lookup"><span data-stu-id="798d3-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="798d3-107">Функции создания и доступа</span><span class="sxs-lookup"><span data-stu-id="798d3-107">Creation/Access Functions</span></span>



| <span data-ttu-id="798d3-108">Функция</span><span class="sxs-lookup"><span data-stu-id="798d3-108">Function</span></span>                                      | <span data-ttu-id="798d3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="798d3-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="798d3-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="798d3-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="798d3-111">Создает экземпляр объекта Сенс, используя его CLSID.</span><span class="sxs-lookup"><span data-stu-id="798d3-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="798d3-112">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="798d3-112">Interfaces</span></span>



| <span data-ttu-id="798d3-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="798d3-113">Interface</span></span>                            | <span data-ttu-id="798d3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="798d3-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="798d3-115">**исенснетворк**</span><span class="sxs-lookup"><span data-stu-id="798d3-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="798d3-116">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="798d3-116">Default.</span></span> <span data-ttu-id="798d3-117">Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.</span><span class="sxs-lookup"><span data-stu-id="798d3-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="798d3-118">**исенсоннов**</span><span class="sxs-lookup"><span data-stu-id="798d3-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="798d3-119">Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.</span><span class="sxs-lookup"><span data-stu-id="798d3-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="798d3-120">**исенслогон**</span><span class="sxs-lookup"><span data-stu-id="798d3-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="798d3-121">Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.</span><span class="sxs-lookup"><span data-stu-id="798d3-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="798d3-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="798d3-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="798d3-123">Исходящий интерфейс, реализованный объектом приемника в приложении подписчика.</span><span class="sxs-lookup"><span data-stu-id="798d3-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="798d3-124">Доступно в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="798d3-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="798d3-125">См. также</span><span class="sxs-lookup"><span data-stu-id="798d3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="798d3-126">**исенслогон**</span><span class="sxs-lookup"><span data-stu-id="798d3-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="798d3-127">**исенснетворк**</span><span class="sxs-lookup"><span data-stu-id="798d3-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="798d3-128">**исенсоннов**</span><span class="sxs-lookup"><span data-stu-id="798d3-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="798d3-129">О службе уведомлений о системных событиях</span><span class="sxs-lookup"><span data-stu-id="798d3-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 

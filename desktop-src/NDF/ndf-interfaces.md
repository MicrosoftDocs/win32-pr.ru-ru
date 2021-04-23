---
title: Интерфейсы NDF
description: Следующие интерфейсы можно использовать для расширения функциональных возможностей вспомогательных классов Майкрософт, которые определены как расширяемые.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067247"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="b40df-103">Интерфейсы NDF</span><span class="sxs-lookup"><span data-stu-id="b40df-103">NDF Interfaces</span></span>

<span data-ttu-id="b40df-104">Следующие интерфейсы можно использовать для расширения функциональных возможностей вспомогательных классов Майкрософт, которые определены как расширяемые.</span><span class="sxs-lookup"><span data-stu-id="b40df-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="b40df-105">Хотя эта функция не является обязательной для большинства приложений, в некоторых случаях она может предоставлять более конкретные методы диагностики и разрешения.</span><span class="sxs-lookup"><span data-stu-id="b40df-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="b40df-106">Эти интерфейсы и связанные с ними методы предназначены для разработчиков, реализующих собственные вспомогательные классы сторонних разработчиков, расширяющие функциональные возможности NDF.</span><span class="sxs-lookup"><span data-stu-id="b40df-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="b40df-107">Имя_интерфейса</span><span class="sxs-lookup"><span data-stu-id="b40df-107">Interface Name</span></span>                                                 | <span data-ttu-id="b40df-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b40df-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b40df-109">**инетдиагхелпер**</span><span class="sxs-lookup"><span data-stu-id="b40df-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="b40df-110">Вызывается NDF для большинства действий, происходящих во время диагностики.</span><span class="sxs-lookup"><span data-stu-id="b40df-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="b40df-111">**инетдиагхелперекс**</span><span class="sxs-lookup"><span data-stu-id="b40df-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="b40df-112">Вызывается NDF для записи и предоставления сведений, связанных с диагностикой и разрешением проблем, связанных с сетью.</span><span class="sxs-lookup"><span data-stu-id="b40df-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="b40df-113">**инетдиагхелперинфо**</span><span class="sxs-lookup"><span data-stu-id="b40df-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="b40df-114">Вызывается NDF для проверки наличия необходимой информации</span><span class="sxs-lookup"><span data-stu-id="b40df-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="b40df-115">**инетдиагхелперутилфактори**</span><span class="sxs-lookup"><span data-stu-id="b40df-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="b40df-116">Зарезервировано для системного использования.</span><span class="sxs-lookup"><span data-stu-id="b40df-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 





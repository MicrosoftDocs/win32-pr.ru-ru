---
description: Расширенные функции телефонии перечислены по категориям в следующих таблицах.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Справочник по расширенным службам телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673286"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="65917-103">Справочник по расширенным службам телефонии</span><span class="sxs-lookup"><span data-stu-id="65917-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="65917-104">Расширенные функции телефонии перечислены по категориям в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="65917-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="65917-105">Расширенные функции телефонии для устройств графики</span><span class="sxs-lookup"><span data-stu-id="65917-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="65917-106">Функция</span><span class="sxs-lookup"><span data-stu-id="65917-106">Function</span></span>                                                   | <span data-ttu-id="65917-107">Описание</span><span class="sxs-lookup"><span data-stu-id="65917-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65917-108">**линенеготиатикстверсион**</span><span class="sxs-lookup"><span data-stu-id="65917-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="65917-109">Позволяет приложению согласовывать версию расширения для использования с указанным устройством.</span><span class="sxs-lookup"><span data-stu-id="65917-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="65917-110">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="65917-110">Asynchronous.</span></span> |
| [<span data-ttu-id="65917-111">**линедевспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="65917-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="65917-112">Предоставляет поставщикам услуг доступ к функциям для конкретных устройств, которые не предлагаются другими функциями TAPI.</span><span class="sxs-lookup"><span data-stu-id="65917-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="65917-113">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="65917-113">Synchronous.</span></span> |
| [<span data-ttu-id="65917-114">**линедевспеЦификфеатуре**</span><span class="sxs-lookup"><span data-stu-id="65917-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="65917-115">Отправляет функции коммутатора для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="65917-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="65917-116">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="65917-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="65917-117">Расширенные функции телефонии для телефонных устройств</span><span class="sxs-lookup"><span data-stu-id="65917-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="65917-118">Функция</span><span class="sxs-lookup"><span data-stu-id="65917-118">Function</span></span>                                                     | <span data-ttu-id="65917-119">Описание</span><span class="sxs-lookup"><span data-stu-id="65917-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65917-120">**фонедевспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="65917-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="65917-121">Функция экранирования для конкретного устройства, позволяющая использовать зависимые от поставщика расширения.</span><span class="sxs-lookup"><span data-stu-id="65917-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="65917-122">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="65917-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="65917-123">**фоненеготиатикстверсион**</span><span class="sxs-lookup"><span data-stu-id="65917-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="65917-124">Позволяет приложению согласовывать версию расширения для использования с указанным телефонным устройством.</span><span class="sxs-lookup"><span data-stu-id="65917-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="65917-125">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="65917-125">Synchronous.</span></span> |



 

 

 




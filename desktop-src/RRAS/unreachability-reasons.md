---
title: Причины недостижимости
description: В следующей таблице перечислены постоянные значения, указывающие, почему интерфейс недоступен.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070354"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="90573-103">Причины недостижимости</span><span class="sxs-lookup"><span data-stu-id="90573-103">Unreachability Reasons</span></span>

<span data-ttu-id="90573-104">В следующей таблице перечислены постоянные значения, указывающие, почему интерфейс недоступен.</span><span class="sxs-lookup"><span data-stu-id="90573-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="90573-105">Значение</span><span class="sxs-lookup"><span data-stu-id="90573-105">Value</span></span>                                       | <span data-ttu-id="90573-106">Значение</span><span class="sxs-lookup"><span data-stu-id="90573-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90573-107">\_Администратор интерфейса \_ MPR \_ отключен</span><span class="sxs-lookup"><span data-stu-id="90573-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="90573-108">Администратор отключил интерфейс.</span><span class="sxs-lookup"><span data-stu-id="90573-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="90573-109">\_ \_ сбой подключения к ИНТЕРФЕЙСу MPR \_</span><span class="sxs-lookup"><span data-stu-id="90573-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="90573-110">Предыдущая попытка соединения завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="90573-110">The previous connection attempt failed.</span></span> <span data-ttu-id="90573-111">Взгляните на элемент **двластеррор** для кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="90573-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="90573-112">\_ограничение на \_ количество подключений \_ \_ многопротокольного интерфейса</span><span class="sxs-lookup"><span data-stu-id="90573-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="90573-113">Исходящие звонки в настоящее время не разрешены.</span><span class="sxs-lookup"><span data-stu-id="90573-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="90573-114">не \_ \_ хватает \_ \_ ресурсов многопротокольного интерфейса</span><span class="sxs-lookup"><span data-stu-id="90573-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="90573-115">Нет доступных портов или устройств для использования.</span><span class="sxs-lookup"><span data-stu-id="90573-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="90573-116">\_служба интерфейса \_ MPR \_ приостановлена</span><span class="sxs-lookup"><span data-stu-id="90573-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="90573-117">Служба приостановлена.</span><span class="sxs-lookup"><span data-stu-id="90573-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="90573-118">многопротокольный \_ интерфейс \_ без \_ \_ смысла</span><span class="sxs-lookup"><span data-stu-id="90573-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="90573-119">Сетевой кабель отключен от сетевой карты.</span><span class="sxs-lookup"><span data-stu-id="90573-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="90573-120">\_интерфейс MPR \_ без \_ устройства</span><span class="sxs-lookup"><span data-stu-id="90573-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="90573-121">Сетевая карта удалена с компьютера.</span><span class="sxs-lookup"><span data-stu-id="90573-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="90573-122">См. также</span><span class="sxs-lookup"><span data-stu-id="90573-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90573-123">**Многопротокольный \_ интерфейс \_ 0**</span><span class="sxs-lookup"><span data-stu-id="90573-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="90573-124">**\_Интерфейс MPR \_ 1**</span><span class="sxs-lookup"><span data-stu-id="90573-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="90573-125">**MIB \_ ифров**</span><span class="sxs-lookup"><span data-stu-id="90573-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="90573-126">**MIB \_ ифстатус**</span><span class="sxs-lookup"><span data-stu-id="90573-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 
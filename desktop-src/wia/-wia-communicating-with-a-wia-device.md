---
description: Когда поток активно взаимодействует с устройством для получения изображений (WIA) (например, передача данных или запись свойств устройства) WIA &\# 0034; locks&\# 0034; устройство.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Взаимодействие с устройством WIA в нескольких потоках или приложениях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264534"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a><span data-ttu-id="c597d-103">Взаимодействие с устройством WIA в нескольких потоках или приложениях</span><span class="sxs-lookup"><span data-stu-id="c597d-103">Communicating with a WIA Device in Multiple Threads or Applications</span></span>

<span data-ttu-id="c597d-104">Когда поток активно взаимодействует с устройством для получения изображений (WIA) (например, передача данных или запись свойств устройства), WIA блокирует устройство.</span><span class="sxs-lookup"><span data-stu-id="c597d-104">When a thread is actively communicating with a Windows Image Acquisition (WIA) device (for example, transferring data or writing device properties) WIA "locks" the device.</span></span> <span data-ttu-id="c597d-105">Если устройство заблокировано, другие потоки или процессы не могут активно взаимодействовать с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="c597d-105">When a device is locked, no other threads or processes can actively communicate with that device.</span></span>

<span data-ttu-id="c597d-106">WIA не запрещает нескольким потокам или процессам поддерживать соединения с одним устройством.</span><span class="sxs-lookup"><span data-stu-id="c597d-106">WIA does not prohibit multiple threads or processes from maintaining connections to a single device.</span></span> <span data-ttu-id="c597d-107">Это значит, что устройство блокируется только во время фактического взаимодействия, и в двух или нескольких приложениях одновременно может быть выбрано одно устройство.</span><span class="sxs-lookup"><span data-stu-id="c597d-107">That is, a device is locked only during the actual communication, and two or more applications can simultaneously have a single device selected.</span></span>

<span data-ttu-id="c597d-108">WIA создает отдельное дерево элементов каждый раз, когда любой поток или приложение вызывает [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) или [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md) для создания экземпляра этого устройства.</span><span class="sxs-lookup"><span data-stu-id="c597d-108">WIA creates a separate item tree each time any thread or application calls [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) to create an instance of that device.</span></span> <span data-ttu-id="c597d-109">WIA поддерживает отдельные сведения о состоянии для каждого дерева элементов.</span><span class="sxs-lookup"><span data-stu-id="c597d-109">WIA maintains separate state information for each item tree.</span></span> <span data-ttu-id="c597d-110">Например, если поток создает два экземпляра определенного сканера, он может задать различные разрешения сканирования для двух экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c597d-110">For example, if a thread creates two instances of a particular scanner, it can set different scan resolutions for the two instances.</span></span> <span data-ttu-id="c597d-111">Когда метод [**ивиадататрансфер:: идтжетдата**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) вызывается для конкретного экземпляра, WIA загружает свойства, связанные с этим экземпляром, на устройство, прежде чем будет выполняться фактическое сканирование.</span><span class="sxs-lookup"><span data-stu-id="c597d-111">When [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) is called on a particular instance, WIA loads the properties associated with that instance to the device before the actual scan takes place.</span></span> <span data-ttu-id="c597d-112">Это не влияет на состояние другого экземпляра устройства.</span><span class="sxs-lookup"><span data-stu-id="c597d-112">This does not affect the state of the other instance of the device.</span></span>

<span data-ttu-id="c597d-113">Если в потоке в настоящий момент устройство заблокировано (активно взаимодействует с этим устройством), а другой поток пытается вызвать метод, который активно взаимодействует с устройством, метод возвращает ошибку, \_ которая \_ занята WIA-ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c597d-113">If a thread currently has a device locked (it is actively communicating with that device) and another thread attempts to call a method that actively communicates with the device, the method returns a WIA\_ERROR\_BUSY error.</span></span>

<span data-ttu-id="c597d-114">Как правило, чтение и запись свойств устройств занимает немного времени, что эти операции редко вызывают конфликт.</span><span class="sxs-lookup"><span data-stu-id="c597d-114">Typically, reading and writing device properties takes so little time that these operations rarely cause a conflict.</span></span> <span data-ttu-id="c597d-115">Однако передача данных обычно занимает больше времени и, следовательно, скорее всего, создает конфликты доступа к устройствам.</span><span class="sxs-lookup"><span data-stu-id="c597d-115">Transferring data, however, usually takes longer, and therefore is more likely to create device access conflicts.</span></span> <span data-ttu-id="c597d-116">Это программирование позволяет избежать длительных операций с устройствами (передачи данных) в отдельных потоках в приложении.</span><span class="sxs-lookup"><span data-stu-id="c597d-116">It is sound programming to avoid lengthy device operations (data transfers) concurrently in separate threads within an application.</span></span>

<span data-ttu-id="c597d-117">Приложение никогда не должно считать, что это единственное приложение, взаимодействующее с устройством WIA при запуске.</span><span class="sxs-lookup"><span data-stu-id="c597d-117">An application should never assume that it is the only application that is communicating with a WIA device when it starts.</span></span>

 

 




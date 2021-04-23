---
description: Поддержка телефонных устройств является дополнительным, а не базовым, поэтому поставщики услуг не должны поддерживать телефонные устройства.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Телефонные устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991289"
---
# <a name="phone-devices"></a><span data-ttu-id="41bad-103">Телефонные устройства</span><span class="sxs-lookup"><span data-stu-id="41bad-103">Phone Devices</span></span>

<span data-ttu-id="41bad-104">Поддержка телефонных устройств является дополнительным, а не базовым, поэтому поставщики услуг не должны поддерживать телефонные устройства.</span><span class="sxs-lookup"><span data-stu-id="41bad-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="41bad-105">Как и класс линейного устройства — это абстракция физического устройства, класс телефонного устройства представляет независимую от устройства абстракцию телефонного набора.</span><span class="sxs-lookup"><span data-stu-id="41bad-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="41bad-106">TAPI рассматривает устройства линий и телефонов как устройства, независимые друг от друга.</span><span class="sxs-lookup"><span data-stu-id="41bad-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="41bad-107">Иными словами, вы можете использовать телефон (устройство) без использования связанной линии, и вы можете использовать линию (устройство) без использования телефона.</span><span class="sxs-lookup"><span data-stu-id="41bad-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="41bad-108">Поставщики услуг, полностью реализующие эту независимость, могут предлагать использовать эти устройства, не определенные традиционными протоколами телефонии.</span><span class="sxs-lookup"><span data-stu-id="41bad-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="41bad-109">Например, человек может использовать телефон рабочего стола в качестве звукового устройства аудио для записи или воспроизведения голоса, возможно, без знания о том, что телефон используется.</span><span class="sxs-lookup"><span data-stu-id="41bad-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="41bad-110">В такой реализации при поднятии локальной телефонной трубки не нужно автоматически передавать сигнал оффхук на коммутатор.</span><span class="sxs-lookup"><span data-stu-id="41bad-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="41bad-111">Эта независимость также позволяет приложению звонить на местный телефон так, чтобы оно не зависело от входящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="41bad-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="41bad-112">Возможности поставщиков услуг ограничены возможностями оборудования и программного обеспечения, используемого для соединения коммутатора, телефона и компьютера.</span><span class="sxs-lookup"><span data-stu-id="41bad-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="41bad-113">TAPI включает функции для получения возможностей устройства, которые позволяют клиентам определить, поддерживается ли такая модель использования.</span><span class="sxs-lookup"><span data-stu-id="41bad-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="41bad-114">В этом разделе описываются телефонные устройства и объясняется, как использовать функции телефонии TAPI для доступа к этим устройствам.</span><span class="sxs-lookup"><span data-stu-id="41bad-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="41bad-115">Телефонное устройство</span><span class="sxs-lookup"><span data-stu-id="41bad-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="41bad-116">Инициализация и завершение работы</span><span class="sxs-lookup"><span data-stu-id="41bad-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 




---
description: После определения возможностей телефонного устройства приложение должно открыть устройство, прежде чем оно сможет получить доступ к функциям на этом телефоне.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Открытие и закрытие телефонных устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673379"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="4021e-103">Открытие и закрытие телефонных устройств</span><span class="sxs-lookup"><span data-stu-id="4021e-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="4021e-104">После определения возможностей телефонного устройства приложение должно открыть устройство, прежде чем оно сможет получить доступ к функциям на этом телефоне.</span><span class="sxs-lookup"><span data-stu-id="4021e-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="4021e-105">После успешного открытия телефонного устройства приложение возвращает маркер, представляющий открытый телефон.</span><span class="sxs-lookup"><span data-stu-id="4021e-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="4021e-106">Телефонное устройство можно открыть в разных режимах, тем самым предоставляя структурированный способ совместного использования телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="4021e-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="4021e-107">Функция [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) открывает указанное телефонное устройство, чтобы предоставить приложению доступ к функциям на телефоне.</span><span class="sxs-lookup"><span data-stu-id="4021e-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="4021e-108">Телефонное устройство определяется как **фонеопен** с помощью идентификатора устройства, который передается как параметр *двдевицеид* .</span><span class="sxs-lookup"><span data-stu-id="4021e-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 




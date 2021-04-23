---
title: Обновление переносных устройств
description: Обновление переносных устройств
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Интернет-магазины проигрывателя Windows Media, обновление переносных устройств
- Интернет-магазины, обновление переносных устройств
- Тип 1 Интернет-магазины, обновление переносных устройств
- Интернет-магазины проигрывателя Windows Media, портативные устройства
- Интернет-магазины, портативные устройства
- Тип 1 Интернет-магазины, портативные устройства
- Обновление переносных устройств
- переносные устройства, обновление
- портативные устройства, Интернет-магазины проигрывателя Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336263"
---
# <a name="updating-portable-devices"></a><span data-ttu-id="a0f09-112">Обновление переносных устройств</span><span class="sxs-lookup"><span data-stu-id="a0f09-112">Updating Portable Devices</span></span>

<span data-ttu-id="a0f09-113">Проигрыватель Windows Media позволяет пользователям синхронизировать мультимедийное содержимое с портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="a0f09-113">Windows Media Player enables users to synchronize digital media content with portable devices.</span></span> <span data-ttu-id="a0f09-114">Это может быть музыкальное содержимое, приобретенное или арендованное в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="a0f09-114">This can include music content purchased or rented from an online store.</span></span> <span data-ttu-id="a0f09-115">В некоторых обстоятельствах поставщики интернет-магазинов могут захотеть написать код для работы на подключенном портативном устройстве в рамках управления содержимым, предоставленным магазином.</span><span class="sxs-lookup"><span data-stu-id="a0f09-115">Under some circumstances, online store providers might want to write code to work on a connected portable device as part of managing content provided by the store.</span></span> <span data-ttu-id="a0f09-116">Чтобы предоставить подключаемому модулю Интернет-магазина возможность работать с подключенным устройством, проигрыватель Windows Media вызывает [ивмпконтентпартнер:: упдатедевице](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) и предоставляет каноническое имя переносимого устройства.</span><span class="sxs-lookup"><span data-stu-id="a0f09-116">To give the online store plug-in the opportunity to work with a connected device, Windows Media Player calls [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) and provides the canonical name of the portable device.</span></span> <span data-ttu-id="a0f09-117">Если код подключаемого модуля определяет, что часть работы должна быть выполнена на подключенном устройстве, перед продолжением работы необходимо немедленно вернуть значение S \_ ОК из вызова в **упдатедевице** .</span><span class="sxs-lookup"><span data-stu-id="a0f09-117">If the plug-in code determines that some work must be done with the connected device, it must immediately return S\_OK from the call to **UpdateDevice** before proceeding to do the work.</span></span> <span data-ttu-id="a0f09-118">Если нет работы, подключаемый модуль должен вернуть код ошибки.</span><span class="sxs-lookup"><span data-stu-id="a0f09-118">If there is no work to do, the plug-in should return an error code.</span></span>

<span data-ttu-id="a0f09-119">Когда подключаемый модуль завершит работу с устройством, он должен вызвать [ивмпконтентпартнеркаллбакк:: упдатедевицекомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) , чтобы уведомить проигрыватель Windows Media о том, что устройство доступно.</span><span class="sxs-lookup"><span data-stu-id="a0f09-119">When the plug-in has finished using the device, it must call [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) to notify Windows Media Player that the device is available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0f09-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a0f09-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f09-121">**Справка по программированию для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="a0f09-121">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 





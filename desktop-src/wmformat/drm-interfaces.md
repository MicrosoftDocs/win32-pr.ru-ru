---
title: Интерфейсы клиента DRM Microsoft Windows Media
description: Интерфейсы клиента DRM Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK, интерфейсы
- Управление цифровыми правами (DRM), интерфейсы
- DRM (Управление цифровыми правами), интерфейсы
- Расширенные API клиента DRM, интерфейсы
- Расширенные API клиента, интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414456"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="615e0-108">Интерфейсы клиента DRM Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="615e0-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="615e0-109">В следующей таблице описаны интерфейсы, поддерживаемые клиентскими API Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="615e0-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="615e0-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="615e0-110">Interface</span></span>                                                                    | <span data-ttu-id="615e0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="615e0-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="615e0-112">**идрмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="615e0-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="615e0-113">Предоставляет определение для обратного вызова состояния, которое можно реализовать для выполнения асинхронных операций DRM.</span><span class="sxs-lookup"><span data-stu-id="615e0-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="615e0-114">**ивмдрмдекрипт**</span><span class="sxs-lookup"><span data-stu-id="615e0-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="615e0-115">Предоставляет метод для расшифровки содержимого.</span><span class="sxs-lookup"><span data-stu-id="615e0-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="615e0-116">**ивмдрменкрипт**</span><span class="sxs-lookup"><span data-stu-id="615e0-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="615e0-117">Предоставляет метод для шифрования данных на месте.</span><span class="sxs-lookup"><span data-stu-id="615e0-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="615e0-118">**ивмдрменкриптскаттер**</span><span class="sxs-lookup"><span data-stu-id="615e0-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="615e0-119">Шифрует данные из несмежных блоков.</span><span class="sxs-lookup"><span data-stu-id="615e0-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="615e0-120">**ивмдрмевентженератор**</span><span class="sxs-lookup"><span data-stu-id="615e0-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="615e0-121">Расширение интерфейса **имфмедиаевентженератор** , предоставляющего метод для отмены асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="615e0-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="615e0-122">**ивмдрминдивидуализатионстатус**</span><span class="sxs-lookup"><span data-stu-id="615e0-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="615e0-123">Включает получение дополнительных сведений о состоянии выполнения индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="615e0-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="615e0-124">**ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="615e0-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="615e0-125">Представляет одну или несколько лицензий в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="615e0-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="615e0-126">**ивмдрмлиценсебаккупресторестатус**</span><span class="sxs-lookup"><span data-stu-id="615e0-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="615e0-127">Включает получение подробных сведений о состоянии операции резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="615e0-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="615e0-128">**ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="615e0-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="615e0-129">Включает операции управления для локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="615e0-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="615e0-130">**ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="615e0-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="615e0-131">Предоставляет дополнительные возможности управления для локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="615e0-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="615e0-132">**ивмдрмлиценсекуери**</span><span class="sxs-lookup"><span data-stu-id="615e0-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="615e0-133">Позволяет приложениям запрашивать права и состояние лицензии для защищенного файла.</span><span class="sxs-lookup"><span data-stu-id="615e0-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="615e0-134">**ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="615e0-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="615e0-135">Предоставляет методы, необходимые для создания приложения-получателя DRM Microsoft Windows Media для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="615e0-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="615e0-136">**ивмдрмнеттрансмиттер**</span><span class="sxs-lookup"><span data-stu-id="615e0-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="615e0-137">Предоставляет методы, необходимые для создания приложения для передатчика сетевых устройств Microsoft Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="615e0-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="615e0-138">**ивмдрмнонсилентлиценсеакуиситион**</span><span class="sxs-lookup"><span data-stu-id="615e0-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="615e0-139">Предоставляет методы, обеспечивающие получение лицензий с вмешательством пользователя.</span><span class="sxs-lookup"><span data-stu-id="615e0-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="615e0-140">**ивмдрмпровидер**</span><span class="sxs-lookup"><span data-stu-id="615e0-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="615e0-141">Создает другие объекты расширенных API-интерфейсов клиента DRM Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="615e0-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="615e0-142">**ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="615e0-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="615e0-143">Управляет различными процессами, связанными с безопасностью, для клиентского компьютера и подсистемы DRM.</span><span class="sxs-lookup"><span data-stu-id="615e0-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="615e0-144">**ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="615e0-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="615e0-145">Управляет отзывом и обновлением компонентов.</span><span class="sxs-lookup"><span data-stu-id="615e0-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="615e0-146">**ивмсекуребуффер**</span><span class="sxs-lookup"><span data-stu-id="615e0-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="615e0-147">Включает шифрование и расшифровку буферов.</span><span class="sxs-lookup"><span data-stu-id="615e0-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="615e0-148">См. также</span><span class="sxs-lookup"><span data-stu-id="615e0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="615e0-149">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="615e0-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 





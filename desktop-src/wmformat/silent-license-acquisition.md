---
title: Автоматическое получение лицензий
description: Автоматическое получение лицензий
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Пакет SDK для формата Windows Media, автоматическое получение лицензий
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), автоматическое получение лицензий
- DRM (Управление цифровыми правами), автоматическое получение лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Расширенные API клиента DRM, автоматическое получение лицензий
- Расширенные API клиента, автоматическое получение лицензий
- Автоматическое получение лицензий
- лицензии, получение бесшумной лицензии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068262"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="8b528-113">Автоматическое получение лицензий</span><span class="sxs-lookup"><span data-stu-id="8b528-113">Silent License Acquisition</span></span>

<span data-ttu-id="8b528-114">Для получения бесшумной лицензии требуется только один вызов метода, который асинхронно обрабатывает все сетевые соединения с сервером лицензий.</span><span class="sxs-lookup"><span data-stu-id="8b528-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="8b528-115">Этот тип приобретения лицензий обычно используется как ответ конечного пользователя, пытающегося получить доступ к защищенному содержимому, например, при попытке воспроизвести защищенный файл в приложении проигрывателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8b528-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="8b528-116">Поскольку получение лицензии без уведомления получает лицензию с одним вызовом, его нельзя использовать, если требуется дополнительный ввод пользователя, например оплата содержимого.</span><span class="sxs-lookup"><span data-stu-id="8b528-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="8b528-117">Для автоматического приобретения лицензий выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b528-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="8b528-118">Вызовите метод [**ивмдрмлиценсеманажемент:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="8b528-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="8b528-119">Передайте заголовок DRM из защищенного файла в качестве параметра *бстрхеадердата* .</span><span class="sxs-lookup"><span data-stu-id="8b528-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="8b528-120">Укажите, какие права вы хотите предоставить лицензии в параметре *бстрактионс* .</span><span class="sxs-lookup"><span data-stu-id="8b528-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="8b528-121">Наконец, задайте для параметра *dwFlags* значение " \_ Автоматическая установка лицензии на получение WMDRM" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8b528-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="8b528-122">События ловушек для интерфейса [**ивмдрмлиценсеманажемент**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="8b528-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="8b528-123">При получении события **мевмдрмлиценсеаккуиситионкомплетед** проверьте его код возврата, вызвав метод **имфмедиаевент::-Status** , который описан в документации по Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b528-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="8b528-124">Если полученное значение **HRESULT** является кодом успешного выполнения, то лицензия была успешно скачана и находится в локальном хранилище лицензий, готовом к использованию.</span><span class="sxs-lookup"><span data-stu-id="8b528-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b528-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8b528-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b528-126">**Получение лицензий**</span><span class="sxs-lookup"><span data-stu-id="8b528-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="8b528-127">**Использование модели событий Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="8b528-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 





---
title: Получение лицензий без уведомления
description: Получение лицензий без уведомления
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Пакет SDK для формата Windows Media, неавтоматическая получение лицензий
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), неавтоматическая получение лицензий
- DRM (Управление цифровыми правами), неавтоматическая получение лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Расширенные API клиента DRM, неавтоматическое получение лицензий
- Расширенные API клиента, получение лицензий без уведомления
- получение лицензий без уведомления
- лицензии, неавтоматическая получение лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532441"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="56a26-113">Получение лицензий без уведомления</span><span class="sxs-lookup"><span data-stu-id="56a26-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="56a26-114">Неавтоматическое получение лицензий позволяет поставщику лицензий взаимодействовать с конечным пользователем через веб-страницу в качестве промежуточного шага в процессе получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="56a26-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="56a26-115">Получение лицензии без уведомления инициируется в ответ на попытку доступа пользователя к защищенному содержимому.</span><span class="sxs-lookup"><span data-stu-id="56a26-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="56a26-116">Чтобы выполнить неавтоматическую процедуру приобретения лицензий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56a26-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="56a26-117">Вызовите метод [**ивмдрмлиценсеманажемент:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="56a26-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="56a26-118">Передайте заголовок DRM из защищенного файла в качестве параметра *бстрхеадердата* .</span><span class="sxs-lookup"><span data-stu-id="56a26-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="56a26-119">Укажите, какие права вы хотите предоставить лицензии в параметре *бстрактионс* .</span><span class="sxs-lookup"><span data-stu-id="56a26-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="56a26-120">Наконец, присвойте параметру *dwFlags* значение WMDRM для \_ \_ \_ неавтоматической лицензии.</span><span class="sxs-lookup"><span data-stu-id="56a26-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="56a26-121">События ловушек для интерфейса **ивмдрмлиценсеманажемент** .</span><span class="sxs-lookup"><span data-stu-id="56a26-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="56a26-122">При получении события **мевмдрмлиценсеаккуиситионкомплетед** получите связанное с ним значение, вызвав **Имфмедиаевент:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="56a26-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="56a26-123">Значение должно иметь тип VT \_ Unknown, указатель на интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="56a26-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="56a26-124">Вызовите метод **QueryInterface** интерфейса **IUnknown** , полученного на шаге 2, чтобы получить интерфейс [**ивмдрмнонсилентлиценсеакуиситион**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="56a26-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="56a26-125">Вызовите [**ивмдрмнонсилентлиценсеакуиситион:: Challenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) , чтобы получить запрос лицензии.</span><span class="sxs-lookup"><span data-stu-id="56a26-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="56a26-126">Также вызовите [**ивмдрмнонсилентлиценсеакуиситион:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) , если у вас еще нет URL-адреса сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="56a26-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="56a26-127">Отправьте запрос на веб-страницу, указанную URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="56a26-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56a26-128">См. также</span><span class="sxs-lookup"><span data-stu-id="56a26-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a26-129">**Получение лицензий**</span><span class="sxs-lookup"><span data-stu-id="56a26-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="56a26-130">**Использование модели событий Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="56a26-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 





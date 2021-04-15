---
title: Предварительная Поставка лицензий
description: Предварительная Поставка лицензий
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Пакет SDK для Windows Media Format, предварительная поставка лицензий
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), предварительная доставка лицензий
- DRM (Управление цифровыми правами), предварительная поставка лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Расширенные API клиента DRM, предварительная доставка лицензий
- Расширенные API клиента, предварительная доставка лицензий
- Предварительная Поставка лицензий
- лицензии, предварительная доставка лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654337"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="22850-113">Предварительная Поставка лицензий</span><span class="sxs-lookup"><span data-stu-id="22850-113">License Pre-Delivery</span></span>

<span data-ttu-id="22850-114">Предварительная Доставка лицензий — это процесс, используемый для принудительного получения лицензий на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="22850-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="22850-115">Распространенным сценарием использования предварительной доставки является ситуация, когда пользователь подписывается на музыкальную службу.</span><span class="sxs-lookup"><span data-stu-id="22850-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="22850-116">Без предоставления лицензий, прежде чем они понадобятся, пользователю придется ожидать приобретения лицензий для каждой новой песни.</span><span class="sxs-lookup"><span data-stu-id="22850-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="22850-117">Поскольку предварительная доставка не выполняется в ответ на попытку доступа, она обычно выполняется только владельцем содержимого.</span><span class="sxs-lookup"><span data-stu-id="22850-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="22850-118">Это значит, что вы можете предварительно доставить лицензии только за содержимое, которое вы контролируете.</span><span class="sxs-lookup"><span data-stu-id="22850-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="22850-119">Процесс предварительной доставки — это координация между клиентским компонентом и сервером лицензирования, созданным с помощью объектов пакета SDK Windows Media Digital Rights Management.</span><span class="sxs-lookup"><span data-stu-id="22850-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="22850-120">Предварительная Доставка лицензий аналогична [приобретению Неавтоматическых лицензий](non-silent-license-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="22850-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="22850-121">Выполните те же действия, за исключением того, что у вас нет заголовка DRM для передачи в [**ивмдрмлиценсеманажемент:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span><span class="sxs-lookup"><span data-stu-id="22850-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="22850-122">Метод создаст запрос, не относящийся к содержимому, который можно отправить на сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="22850-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="22850-123">Кроме того, можно использовать [Диспетчер прав Windows Media](/previous-versions//bb676133(v=technet.10)) для предварительной доставки лицензий.</span><span class="sxs-lookup"><span data-stu-id="22850-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22850-124">См. также</span><span class="sxs-lookup"><span data-stu-id="22850-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22850-125">**Получение лицензий**</span><span class="sxs-lookup"><span data-stu-id="22850-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="22850-126">**Использование модели событий Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="22850-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 
---
title: Перечисление лицензий в локальном хранилище лицензий
description: Перечисление лицензий в локальном хранилище лицензий
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Пакет SDK для Windows Media Format, перечисление лицензий
- Пакет SDK для Windows Media Format, лицензии
- Пакет SDK Windows Media Format, локальное хранилище лицензий
- Управление цифровыми правами (DRM), перечисление лицензий
- DRM (Управление цифровыми правами), перечисление лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), локальное хранилище лицензий
- DRM (Управление цифровыми правами), локальное хранилище лицензий
- Расширенные API клиента DRM, перечисление лицензий
- Расширенные API клиента, перечисление лицензий
- Расширенные API клиента DRM, лицензии
- Расширенные API клиента, лицензии
- Расширенные API клиента DRM, локальное хранилище лицензий
- Расширенные API клиента, локальное хранилище лицензий
- лицензии, перечисление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410768"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="bb8db-119">Перечисление лицензий в локальном хранилище лицензий</span><span class="sxs-lookup"><span data-stu-id="bb8db-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="bb8db-120">Перечисление — это процесс получения сведений о лицензиях в локальном хранилище лицензий с пошаговым выполнением по одному.</span><span class="sxs-lookup"><span data-stu-id="bb8db-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="bb8db-121">Вы можете создать перечисление лицензий, вызвав метод [**ивмдрмлиценсеманажемент:: креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="bb8db-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="bb8db-122">Наиболее распространенной причиной перечисления лицензий в магазине является поиск определенной лицензии для расшифровки какого-либо содержимого.</span><span class="sxs-lookup"><span data-stu-id="bb8db-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="bb8db-123">Интерфейс [**ивмдрмлиценсе**](iwmdrmlicense.md) выступает в качестве портала к отдельным результатам лицензии и в качестве перечислителя.</span><span class="sxs-lookup"><span data-stu-id="bb8db-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="bb8db-124">При создании перечисления лицензий первая лицензия в списке загружается в интерфейс **ивмдрмлиценсе** .</span><span class="sxs-lookup"><span data-stu-id="bb8db-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="bb8db-125">Большинство методов **ивмдрмлиценсе** позволяют получать сведения о лицензии или создавать объекты для шифрования и расшифровки содержимого на основе лицензии.</span><span class="sxs-lookup"><span data-stu-id="bb8db-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="bb8db-126">Однако существует два метода управления перечислением: [**GetNext**](iwmdrmlicense-getnext.md) и [**ресетенумератион**](iwmdrmlicense-resetenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="bb8db-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="bb8db-127">**OnNext** загружает следующую лицензию из списка в интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bb8db-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="bb8db-128">**Ресетенумератион** возвращает перечисление в состояние, в котором он находился при первоначальном создании.</span><span class="sxs-lookup"><span data-stu-id="bb8db-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="bb8db-129">При сбросе перечисления первая лицензия в списке загружается обратно в интерфейс **ивмдрмлиценсе** .</span><span class="sxs-lookup"><span data-stu-id="bb8db-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="bb8db-130">Когда вы достигли последней лицензии в списке, следующий вызов метода **GetNext ВОЗВРАЩАЕТ ошибку** "больше \_ нет элементов" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bb8db-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="bb8db-131">Если приложение выполняет действие с содержимым, которое охватывает DRM, следует проверить лицензии в локальном хранилище лицензий на наличие прав и других ограничивающих факторов, таких как уровни защиты выходных данных (Оплс).</span><span class="sxs-lookup"><span data-stu-id="bb8db-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb8db-132">См. также</span><span class="sxs-lookup"><span data-stu-id="bb8db-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8db-133">**Получение сведений из лицензий в локальном хранилище лицензий**</span><span class="sxs-lookup"><span data-stu-id="bb8db-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 





---
title: Интерфейс Ивмдрмлиценсеманажемент
description: Интерфейс Ивмдрмлиценсеманажемент предоставляет методы, выполняющие общие операции, связанные с локальным хранилищем лицензий. Чтобы получить экземпляр этого интерфейса, вызовите Ивмдрмпровидер CreateObject. Передайте IID \_ ивмдрмлиценсеманажемент в качестве параметра riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Формат Windows Media в интерфейсе Ивмдрмлиценсеманажемент
- Ивмдрмлиценсеманажемент интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333936"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="a6123-106">Интерфейс Ивмдрмлиценсеманажемент</span><span class="sxs-lookup"><span data-stu-id="a6123-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="a6123-107">Интерфейс **ивмдрмлиценсеманажемент** предоставляет методы, выполняющие общие операции, связанные с локальным хранилищем лицензий.</span><span class="sxs-lookup"><span data-stu-id="a6123-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="a6123-108">Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="a6123-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="a6123-109">Передайте **IID \_ ивмдрмлиценсеманажемент** в качестве параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="a6123-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="a6123-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="a6123-110">Members</span></span>

<span data-ttu-id="a6123-111">Интерфейс **ивмдрмлиценсеманажемент** наследует от [**ивмдрмевентженератор**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="a6123-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="a6123-112">**Ивмдрмлиценсеманажемент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a6123-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="a6123-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a6123-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6123-114">Методы</span><span class="sxs-lookup"><span data-stu-id="a6123-114">Methods</span></span>

<span data-ttu-id="a6123-115">Интерфейс **ивмдрмлиценсеманажемент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a6123-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="a6123-116">Метод</span><span class="sxs-lookup"><span data-stu-id="a6123-116">Method</span></span>                                                                                               | <span data-ttu-id="a6123-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a6123-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6123-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="a6123-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="a6123-119">Асинхронно получает лицензию по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="a6123-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="a6123-120">**баккуплиценсес**</span><span class="sxs-lookup"><span data-stu-id="a6123-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="a6123-121">Создает резервную копию лицензий в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="a6123-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="a6123-122">**клеанлиценсесторе**</span><span class="sxs-lookup"><span data-stu-id="a6123-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="a6123-123">Удаляет помеченные лицензии из хранилища лицензий и выполняет дефрагментацию хранилища для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="a6123-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="a6123-124">**креателиценсинумератион**</span><span class="sxs-lookup"><span data-stu-id="a6123-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="a6123-125">Создает объект перечислителя лицензий, заполненный сведениями о лицензиях на основе значений параметров.</span><span class="sxs-lookup"><span data-stu-id="a6123-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="a6123-126">**креателиценсеревокатиончалленже**</span><span class="sxs-lookup"><span data-stu-id="a6123-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="a6123-127">Создает запрос отзыва лицензии.</span><span class="sxs-lookup"><span data-stu-id="a6123-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="a6123-128">**делетелиценсе**</span><span class="sxs-lookup"><span data-stu-id="a6123-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="a6123-129">Удаляет лицензию из временного локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="a6123-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="a6123-130">**мониторлиценсеаккуиситион**</span><span class="sxs-lookup"><span data-stu-id="a6123-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="a6123-131">Инициирует мониторинг процесса получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="a6123-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="a6123-132">**процесслиценседелетионмессаже**</span><span class="sxs-lookup"><span data-stu-id="a6123-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="a6123-133">Удаляет лицензию, которая была импортирована для содержимого, изначально защищенного с помощью другой системы защиты содержимого.</span><span class="sxs-lookup"><span data-stu-id="a6123-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="a6123-134">**процесслиценсеревокатионреспонсе**</span><span class="sxs-lookup"><span data-stu-id="a6123-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="a6123-135">Отменяет лицензии из локального хранилища лицензий.</span><span class="sxs-lookup"><span data-stu-id="a6123-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="a6123-136">**ресторелиценсес**</span><span class="sxs-lookup"><span data-stu-id="a6123-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="a6123-137">Восстановление ранее резервных копий лицензий.</span><span class="sxs-lookup"><span data-stu-id="a6123-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="a6123-138">**сторелиценсе**</span><span class="sxs-lookup"><span data-stu-id="a6123-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="a6123-139">Добавляет лицензию в локальное хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="a6123-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="a6123-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6123-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6123-141">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="a6123-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a6123-142">**ивмдрмевентженератор**</span><span class="sxs-lookup"><span data-stu-id="a6123-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 






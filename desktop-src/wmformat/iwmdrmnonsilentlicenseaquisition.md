---
title: Интерфейс Ивмдрмнонсилентлиценсеакуиситион
description: Интерфейс Ивмдрмнонсилентлиценсеакуиситион предоставляет методы, обеспечивающие получение лицензий, требующих вмешательства пользователя. Этот интерфейс можно получить, выполнив нестандартное получение лицензий.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Формат Windows Media в интерфейсе Ивмдрмнонсилентлиценсеакуиситион
- Ивмдрмнонсилентлиценсеакуиситион интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792684"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="1bfef-105">Интерфейс Ивмдрмнонсилентлиценсеакуиситион</span><span class="sxs-lookup"><span data-stu-id="1bfef-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="1bfef-106">Интерфейс **ивмдрмнонсилентлиценсеакуиситион** предоставляет методы, обеспечивающие получение лицензий, требующих вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="1bfef-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="1bfef-107">Этот интерфейс можно получить, выполнив нестандартное получение лицензий.</span><span class="sxs-lookup"><span data-stu-id="1bfef-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="1bfef-108">После вызова [**ивмдрмлиценсеманажемент:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) будет создано событие **мевмдрмлиценсеаккуиситионкомплетед** .</span><span class="sxs-lookup"><span data-stu-id="1bfef-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="1bfef-109">Вызовите метод **имфмедиаевент:: GetValue** события, чтобы получить указатель на интерфейс **IUnknown** , для которого можно запросить указатель на экземпляр этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1bfef-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="1bfef-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="1bfef-110">Members</span></span>

<span data-ttu-id="1bfef-111">Интерфейс **ивмдрмнонсилентлиценсеакуиситион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1bfef-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1bfef-112">**Ивмдрмнонсилентлиценсеакуиситион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1bfef-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="1bfef-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1bfef-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1bfef-114">Методы</span><span class="sxs-lookup"><span data-stu-id="1bfef-114">Methods</span></span>

<span data-ttu-id="1bfef-115">Интерфейс **ивмдрмнонсилентлиценсеакуиситион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1bfef-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="1bfef-116">Метод</span><span class="sxs-lookup"><span data-stu-id="1bfef-116">Method</span></span>                                                                | <span data-ttu-id="1bfef-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1bfef-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bfef-118">**Вызов**</span><span class="sxs-lookup"><span data-stu-id="1bfef-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="1bfef-119">Получает запрос лицензии, который должен быть опубликован на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="1bfef-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="1bfef-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="1bfef-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="1bfef-121">Извлекает URL-адрес, на который должен быть опубликован запрос лицензии.</span><span class="sxs-lookup"><span data-stu-id="1bfef-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="1bfef-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bfef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfef-123">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="1bfef-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1bfef-124">**Получение лицензий без уведомления**</span><span class="sxs-lookup"><span data-stu-id="1bfef-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 


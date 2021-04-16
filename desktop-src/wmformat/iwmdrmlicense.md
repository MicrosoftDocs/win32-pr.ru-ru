---
title: Интерфейс Ивмдрмлиценсе
description: Интерфейс Ивмдрмлиценсе представляет список из одной или нескольких лицензий.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Формат Windows Media в интерфейсе Ивмдрмлиценсе
- Ивмдрмлиценсе интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487952"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="1ae0f-105">Интерфейс Ивмдрмлиценсе</span><span class="sxs-lookup"><span data-stu-id="1ae0f-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="1ae0f-106">Интерфейс **ивмдрмлиценсе** представляет список из одной или нескольких лицензий.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="1ae0f-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="1ae0f-107">Members</span></span>

<span data-ttu-id="1ae0f-108">Интерфейс **ивмдрмлиценсе** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1ae0f-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1ae0f-109">**Ивмдрмлиценсе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1ae0f-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="1ae0f-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1ae0f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1ae0f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1ae0f-111">Methods</span></span>

<span data-ttu-id="1ae0f-112">Интерфейс **ивмдрмлиценсе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="1ae0f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="1ae0f-113">Method</span></span>                                                                                   | <span data-ttu-id="1ae0f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1ae0f-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ae0f-115">**канперсист**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="1ae0f-116">Запрашивает возможность сохранения лицензии в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="1ae0f-117">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="1ae0f-118">Создает объект дешифратора, используя параметры текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="1ae0f-119">**креатинкриптор**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="1ae0f-120">Создает объект шифратора, используя параметры текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="1ae0f-121">**креатесекуредекриптор**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="1ae0f-122">Создает объект безопасного дешифратора.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="1ae0f-123">Безопасный дешифратор отличается от обычного дешифратора в том, что расшифровывает содержимое, а затем повторно шифрует его в соответствии с параметрами, заданными в параметрах этого метода.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="1ae0f-124">**жетаналогвидеорестриктионлевелс**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="1ae0f-125">Возвращает все установленные для текущей лицензии ограничения аналогового видео.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="1ae0f-126">**жетинклусионлист**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="1ae0f-127">Извлекает весь список включения для текущей лицензии или цепочки лицензий.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="1ae0f-128">**Лицензия**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="1ae0f-129">Извлекает лицензию как данные язык XML (XML) или Extensible Media Rights (КСМР).</span><span class="sxs-lookup"><span data-stu-id="1ae0f-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1ae0f-130">**жетлиценсепроперти**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="1ae0f-131">Извлекает свойство из текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="1ae0f-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="1ae0f-133">Загружает сведения о следующей лицензии в списке.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="1ae0f-134">**жетаутпутпротектионлевелс**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="1ae0f-135">Извлекает сведения обо всех уровнях защиты выходных данных (Оплс), назначенных лицензии.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="1ae0f-136">**персистлиценсе**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="1ae0f-137">Сохраняет текущую лицензию из временного хранилища в постоянное локальное хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="1ae0f-138">**ресетенумератион**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="1ae0f-139">Сбрасывает список лицензий в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="1ae0f-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="1ae0f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ae0f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae0f-141">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="1ae0f-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 


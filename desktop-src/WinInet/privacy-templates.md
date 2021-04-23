---
title: Шаблоны конфиденциальности (WinInet. h)
description: Ниже приведены уровни конфиденциальности, которые соответствуют правилам принятия, условного принятия или отсутствия приема файлов cookie.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9394068721920836f61871ca42471469fd4c592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493161"
---
# <a name="privacy-templates"></a><span data-ttu-id="b23dc-103">Шаблоны конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="b23dc-103">Privacy Templates</span></span>

<span data-ttu-id="b23dc-104">Ниже приведены уровни конфиденциальности, которые соответствуют правилам принятия, условного принятия или отсутствия приема файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="b23dc-104">The following are privacy levels that equate to rules for accepting, conditionally accepting, or not accepting cookies.</span></span> <span data-ttu-id="b23dc-105">Эти уровни соответствуют уровням предпочтений конфиденциальности, заданным на вкладке Конфиденциальность в свойствах обозревателя.</span><span class="sxs-lookup"><span data-stu-id="b23dc-105">These levels correspond to the privacy preference levels set on the Privacy tab in Internet Options.</span></span> <span data-ttu-id="b23dc-106">Подробные определения см. [в разделе о конфиденциальности в Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) .</span><span class="sxs-lookup"><span data-stu-id="b23dc-106">See [Privacy in Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) for detailed definitions.</span></span>

<dl> <dt>

<span data-ttu-id="b23dc-107"><span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**\_шаблон конфиденциальности \_ без \_ файлов cookie**</span><span class="sxs-lookup"><span data-stu-id="b23dc-107"><span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**PRIVACY\_TEMPLATE\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-108">0</span><span class="sxs-lookup"><span data-stu-id="b23dc-108">0</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-109">Это аналогично **блокировке всех файлов cookie** на ползунке настройки конфиденциальности в **свойствах браузера**.</span><span class="sxs-lookup"><span data-stu-id="b23dc-109">This is the same as **Block All Cookies** on the Privacy Preferences slider bar in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-110"><span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**\_шаблон конфиденциальности \_ высокий**</span><span class="sxs-lookup"><span data-stu-id="b23dc-110"><span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**PRIVACY\_TEMPLATE\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-111">1</span><span class="sxs-lookup"><span data-stu-id="b23dc-111">1</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-112">Это то **же самое, что и** ползунок «настройки конфиденциальности» в окне « **Свойства обозревателя**».</span><span class="sxs-lookup"><span data-stu-id="b23dc-112">This is the same as **High** on the Privacy Preferences slider bar in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-113"><span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**\_шаблон конфиденциальности \_ среднего \_ высокого уровня**</span><span class="sxs-lookup"><span data-stu-id="b23dc-113"><span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**PRIVACY\_TEMPLATE\_MEDIUM\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-114">2</span><span class="sxs-lookup"><span data-stu-id="b23dc-114">2</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-115">Это то **же самое, что \_ и** на ползунке настройки конфиденциальности в **свойствах обозревателя**.</span><span class="sxs-lookup"><span data-stu-id="b23dc-115">This is the same as **Medium\_High** on the Privacy Preferences slider bar in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-116"><span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**\_ \_ средний уровень шаблона конфиденциальности**</span><span class="sxs-lookup"><span data-stu-id="b23dc-116"><span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**PRIVACY\_TEMPLATE\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-117">3</span><span class="sxs-lookup"><span data-stu-id="b23dc-117">3</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-118">Это аналогично **среднему** значению ползунка настройки конфиденциальности в **свойствах обозревателя**.</span><span class="sxs-lookup"><span data-stu-id="b23dc-118">This is the same as **Medium** on the Privacy Preferences slider bar in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-119"><span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**\_шаблон конфиденциальности \_ Medium \_ низкий**</span><span class="sxs-lookup"><span data-stu-id="b23dc-119"><span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**PRIVACY\_TEMPLATE\_MEDIUM\_LOW**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-120">4</span><span class="sxs-lookup"><span data-stu-id="b23dc-120">4</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-121">Это то же самое, **что и** ползунок «настройки конфиденциальности» в окне « **Свойства обозревателя**».</span><span class="sxs-lookup"><span data-stu-id="b23dc-121">This is the same as **Low** on the Privacy Preferences slider bar in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-122"><span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**\_шаблон конфиденциальности \_ низкий**</span><span class="sxs-lookup"><span data-stu-id="b23dc-122"><span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**PRIVACY\_TEMPLATE\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-123">5</span><span class="sxs-lookup"><span data-stu-id="b23dc-123">5</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-124">Это то же самое, что и « **принимать все файлы cookie** » ползунка «параметры конфиденциальности» в окне « **Свойства обозревателя**».</span><span class="sxs-lookup"><span data-stu-id="b23dc-124">This is the same as **Accept All Cookies** on the Privacy Preferences slider bar in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-125"><span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**\_Пользовательский шаблон \_ конфиденциальности**</span><span class="sxs-lookup"><span data-stu-id="b23dc-125"><span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**PRIVACY\_TEMPLATE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-126">100</span><span class="sxs-lookup"><span data-stu-id="b23dc-126">100</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-127">Определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="b23dc-127">User-defined.</span></span> <span data-ttu-id="b23dc-128">Сведения о настройке пользовательских параметров конфиденциальности см. в разделе [Создание пользовательского файла импорта данных о конфиденциальности](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) .</span><span class="sxs-lookup"><span data-stu-id="b23dc-128">See [How to Create a Customized Privacy Import File](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) to understand how to set custom privacy settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-129"><span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**\_Расширенный шаблон \_ конфиденциальности**</span><span class="sxs-lookup"><span data-stu-id="b23dc-129"><span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**PRIVACY\_TEMPLATE\_ADVANCED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-130">101</span><span class="sxs-lookup"><span data-stu-id="b23dc-130">101</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-131">Определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="b23dc-131">User-defined.</span></span> <span data-ttu-id="b23dc-132">Дополнительные параметры задаются в диалоговом окне **Дополнительные параметры конфиденциальности** , доступном на вкладке **Конфиденциальность** в **свойствах обозревателя**.</span><span class="sxs-lookup"><span data-stu-id="b23dc-132">Advanced options are set in the **Advanced Privacy Settings** dialog reachable from the **Privacy** tab in **Internet Options**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b23dc-133"><span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**\_ \_ максимальный размер шаблона конфиденциальности**</span><span class="sxs-lookup"><span data-stu-id="b23dc-133"><span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**PRIVACY\_TEMPLATE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b23dc-134">\_шаблон конфиденциальности \_ низкий</span><span class="sxs-lookup"><span data-stu-id="b23dc-134">PRIVACY\_TEMPLATE\_LOW</span></span>
</dt> <dt>



<span data-ttu-id="b23dc-135">То же, что и **\_ шаблон конфиденциальности \_ низкая**.</span><span class="sxs-lookup"><span data-stu-id="b23dc-135">Same as **PRIVACY\_TEMPLATE\_LOW**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b23dc-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b23dc-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b23dc-137">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="b23dc-137">WinINet does not support server implementations.</span></span> <span data-ttu-id="b23dc-138">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="b23dc-138">In addition, it should not be used from a service.</span></span> <span data-ttu-id="b23dc-139">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="b23dc-139">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b23dc-140">Требования</span><span class="sxs-lookup"><span data-stu-id="b23dc-140">Requirements</span></span>



| <span data-ttu-id="b23dc-141">Требование</span><span class="sxs-lookup"><span data-stu-id="b23dc-141">Requirement</span></span> | <span data-ttu-id="b23dc-142">Значение</span><span class="sxs-lookup"><span data-stu-id="b23dc-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b23dc-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b23dc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b23dc-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b23dc-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b23dc-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b23dc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b23dc-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b23dc-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b23dc-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b23dc-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b23dc-148"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="b23dc-148"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b23dc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b23dc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23dc-150">**привацижетзонепреференцев**</span><span class="sxs-lookup"><span data-stu-id="b23dc-150">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="b23dc-151">**привацисетзонепреференцев**</span><span class="sxs-lookup"><span data-stu-id="b23dc-151">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 


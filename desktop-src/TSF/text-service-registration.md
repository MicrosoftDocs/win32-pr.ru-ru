---
title: Регистрация службы текстового ввода
description: В дополнение к стандартным записям реестра серверной модели COM, служба текстового ввода должна зарегистрироваться в среде текстовых служб (TSF), чтобы она могла быть доступна для использования с приложением.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Платформа текстовых служб (TSF), регистрация
- TSF (платформа текстовых служб), регистрация
- текстовые службы, регистрация
- Платформа текстовых служб (TSF), языковые профили
- TSF (платформа текстовых служб), профили языка
- текстовые службы, языковые профили
- Платформа текстовых служб (TSF), категории
- TSF (платформа текстовых служб), категории
- текстовые службы, категории
- Регистрация текстовых служб
- регистрация профилей языка
- регистрация категорий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487976"
---
# <a name="text-service-registration"></a><span data-ttu-id="829cf-115">Регистрация службы текстового ввода</span><span class="sxs-lookup"><span data-stu-id="829cf-115">Text Service Registration</span></span>

<span data-ttu-id="829cf-116">В дополнение к стандартным записям реестра серверной модели COM, служба текстового ввода должна зарегистрироваться в среде текстовых служб (TSF), чтобы она могла быть доступна для использования с приложением.</span><span class="sxs-lookup"><span data-stu-id="829cf-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="829cf-117">TSF предоставляет интерфейс [итфинпутпроцессорпрофилес](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) и [итфкатегоримгр](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) для упрощения процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="829cf-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="829cf-118">Поставщики текстовых служб также должны предоставлять цифровые подписи в двоичные исполняемые файлы.</span><span class="sxs-lookup"><span data-stu-id="829cf-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="829cf-119">См. статью [Введение в подписывание кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="829cf-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="829cf-120">Регистрация службы текста</span><span class="sxs-lookup"><span data-stu-id="829cf-120">Registering the Text Service</span></span>

<span data-ttu-id="829cf-121">Служба текстового ввода регистрируется в TSF, вызывая [итфинпутпроцессорпрофилес:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) с идентификатором класса текстовой службы.</span><span class="sxs-lookup"><span data-stu-id="829cf-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="829cf-122">Экземпляр интерфейса **итфинпутпроцессорпрофилес** получается путем вызова **CoCreateInstance** с CLSID \_ tf \_ инпутпроцессорпрофилес.</span><span class="sxs-lookup"><span data-stu-id="829cf-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="829cf-123">В следующем примере показано, как создать объект **итфинпутпроцессорпрофилес** и зарегистрировать текстовую службу.</span><span class="sxs-lookup"><span data-stu-id="829cf-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="829cf-124">Итфинпутпроцессорпрофилес:: Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="829cf-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="829cf-125">Регистрация профилей языка</span><span class="sxs-lookup"><span data-stu-id="829cf-125">Registering Language Profiles</span></span>

<span data-ttu-id="829cf-126">Служба текстового ввода доступна только в том случае, если фокус находится в приложении и на языковой панели выбран нужный язык.</span><span class="sxs-lookup"><span data-stu-id="829cf-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="829cf-127">Для упрощения этой процедуры TSF требует, чтобы служба текстового ввода зарегистрировалась для всех поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="829cf-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="829cf-128">Служба текстового интерфейса регистрирует свои языковые профили, вызывая [итфинпутпроцессорпрофилес:: аддлангуажепрофиле](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) с идентификатором класса службы текста, идентификатором языка профиля и **идентификатором GUID** , определенным в текстовой службе, который определяет языковой профиль.</span><span class="sxs-lookup"><span data-stu-id="829cf-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="829cf-129">Можно удалить языковой профиль, вызвав [итфинпутпроцессорпрофилес:: ремовелангуажепрофиле](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span><span class="sxs-lookup"><span data-stu-id="829cf-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="829cf-130">**Итфинпутпроцессорпрофилес:: Unregister** удаляет все языковые профили для службы текстового ввода. При удалении текстовой службы необходимо удалить отдельные языковые профили.</span><span class="sxs-lookup"><span data-stu-id="829cf-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="829cf-131">Регистрация категорий</span><span class="sxs-lookup"><span data-stu-id="829cf-131">Registering Categories</span></span>

<span data-ttu-id="829cf-132">Служба текстового ввода также должна зарегистрировать категорию, к которой применяется служба текстовой службы.</span><span class="sxs-lookup"><span data-stu-id="829cf-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="829cf-133">Например, если служба текстового интерфейса предоставляет сведения об атрибутах, она должна зарегистрировать себя в качестве поставщика атрибута просмотра, вызвав [итфкатегоримгр:: регистеркатегори](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) с идентификатором класса текстового сервиса для первого параметра, GUID \_ тфкат \_ дисплайаттрибутепровидер для второго параметра и идентификатор класса службы текстового ввода для третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="829cf-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="829cf-134">Возможные категории перечислены в разделе [стандартные значения категорий](predefined-category-values.md).</span><span class="sxs-lookup"><span data-stu-id="829cf-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="829cf-135">Удалите ранее зарегистрированные категории, вызвав [итфкатегоримгр:: унрегистеркатегори](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span><span class="sxs-lookup"><span data-stu-id="829cf-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="829cf-136">Итфинпутпроцессорпрофилес:: Unregister удаляет все категории для службы текстового ввода. При удалении текстовой службы необходимо удалить отдельные категории.</span><span class="sxs-lookup"><span data-stu-id="829cf-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 
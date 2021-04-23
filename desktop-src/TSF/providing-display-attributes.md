---
title: Предоставление атрибутов вывода
description: Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Платформа текстовых служб (TSF), атрибуты вывода
- TSF (платформа текстовых служб), атрибуты вывода
- текстовые службы, атрибуты вывода
- атрибуты отображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f59bb64ef4f06df020a40189d273c703768d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681436"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="45e31-107">Предоставление атрибутов вывода</span><span class="sxs-lookup"><span data-stu-id="45e31-107">Providing Display Attributes</span></span>

<span data-ttu-id="45e31-108">Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста.</span><span class="sxs-lookup"><span data-stu-id="45e31-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="45e31-109">Это позволяет предоставить пользователю дополнительные визуальные отзывы.</span><span class="sxs-lookup"><span data-stu-id="45e31-109">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="45e31-110">Например, Текстовая служба проверки орфографии может выделить слово с ошибками с красной подчеркиванием.</span><span class="sxs-lookup"><span data-stu-id="45e31-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="45e31-111">Предоставленные атрибуты экрана определяются структурой [tf \_ дисплайаттрибуте](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) и включают цвет текста, цвет фона текста, стиль подчеркивания, цвет подчеркивания и толщину подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="45e31-111">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="45e31-112">Клиенты, использующие эту информацию об атрибутах вывода, чаще всего являются приложениями, но могут также включать текстовые службы.</span><span class="sxs-lookup"><span data-stu-id="45e31-112">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="45e31-113">Диспетчер TSF подводит между поставщиком атрибута дисплея и клиентом и отслеживает поставщик атрибута дисплея для конкретных атрибутов экрана.</span><span class="sxs-lookup"><span data-stu-id="45e31-113">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="45e31-114">Чтобы предоставить атрибуты вывода, служба текстового ввода должна выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="45e31-114">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="45e31-115">Зарегистрируйте службу текста как поставщик атрибута просмотра, вызвав [итфкатегоримгр:: регистеркатегори](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) с идентификатором класса текстового сервиса для первого параметра, GUID \_ тфкат \_ дисплайаттрибутепровидер для второго параметра и идентификатор класса службы текстового ввода для третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="45e31-115">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="45e31-116">Реализуйте [итфдисплайаттрибутепровидер](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) и сделайте его доступным из фабрики классов.</span><span class="sxs-lookup"><span data-stu-id="45e31-116">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="45e31-117">Реализуйте [иенумтфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) и сделайте его доступным из [Итфдисплайаттрибутепровидер:: енумдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="45e31-117">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="45e31-118">Реализуйте объект [итфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) для каждого типа отображаемого атрибута, предоставляемого службой текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="45e31-118">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="45e31-119">Применение атрибутов вывода</span><span class="sxs-lookup"><span data-stu-id="45e31-119">Applying the Display Attributes</span></span>

<span data-ttu-id="45e31-120">Текстовая служба должна применять атрибут дисплея к диапазону текста.</span><span class="sxs-lookup"><span data-stu-id="45e31-120">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="45e31-121">Служба текстового ввода может изменять значение свойства только во время сеанса изменения, доступного для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="45e31-121">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="45e31-122">При условии, что это происходит в сеансе редактирования для чтения и записи, атрибут дисплея применяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="45e31-122">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="45e31-123">Получите объект [итфранже](/windows/desktop/api/Msctf/nn-msctf-itfrange) , охватывающий текст, к которому будет применен атрибут вывода.</span><span class="sxs-lookup"><span data-stu-id="45e31-123">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="45e31-124">Получите объект [итфпроперти](/windows/desktop/api/Msctf/nn-msctf-itfproperty) для текстовых атрибутов, вызвав [ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) GetObject с \_ атрибутом Prop GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="45e31-124">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="45e31-125">Создайте [тфгуидатом](tfguidatom.md) на основе определяемого службой текстового **интерфейса GUID** идентификатора атрибута, вызвав [итфкатегоримгр:: регистергуид](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="45e31-125">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="45e31-126">Инициализируйте переменную типа VARIANT для VT \_ I4 и задайте для элемента **Лвал** значение **тфгуидатом** , созданное на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="45e31-126">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="45e31-127">Примените атрибут дисплея к диапазону, вызвав [итфпроперти:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) с файлом cookie для чтения и записи, диапазон и вариант, инициализированный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="45e31-127">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="45e31-128">Предоставление объекта сведений о отображаемом атрибуте</span><span class="sxs-lookup"><span data-stu-id="45e31-128">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="45e31-129">Клиент получает объект **итфдисплайаттрибутеинфо** одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="45e31-129">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="45e31-130">Клиент вызывает [итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) с идентификатором **GUID** атрибута дисплея.</span><span class="sxs-lookup"><span data-stu-id="45e31-130">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="45e31-131">При первом вызове **итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо** диспетчер TSF создает экземпляр поставщика отображаемого атрибута, вызывая CoCreateInstance с идентификатором класса, переданным в качестве первого параметра в **Итфкатегоримгр:: регистеркатегори**.</span><span class="sxs-lookup"><span data-stu-id="45e31-131">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="45e31-132">Последующие вызовы **итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо** будут использовать объект поставщика отображаемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="45e31-132">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="45e31-133">Затем Диспетчер TSF вызывает [итфдисплайаттрибутепровидер:: жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) с **идентификатором GUID** атрибута дисплея для получения объекта **итфдисплайаттрибутеинфо** .</span><span class="sxs-lookup"><span data-stu-id="45e31-133">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="45e31-134">Затем Диспетчер TSF передает объект **итфдисплайаттрибутеинфо** обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="45e31-134">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="45e31-135">Клиент вызывает [итфдисплайаттрибутемгр:: енумдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) , чтобы получить объект **иенумтфдисплайаттрибутеинфо** , содержащий все атрибуты вывода, предоставленные всеми поставщиками атрибутов просмотра.</span><span class="sxs-lookup"><span data-stu-id="45e31-135">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="45e31-136">Диспетчер TSF перечисляет каждый поставщик атрибутов экрана и создает экземпляр каждого поставщика, вызывая CoCreateInstance с идентификатором класса, переданным в качестве третьего параметра в **итфкатегоримгр:: регистеркатегори**.</span><span class="sxs-lookup"><span data-stu-id="45e31-136">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="45e31-137">Затем Диспетчер TSF вызывает **итфдисплайаттрибутепровидер:: енумдисплайаттрибутеинфо** каждого поставщика, чтобы получить объект **иенумтфдисплайаттрибутеинфо** , содержащий все атрибуты вывода, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="45e31-137">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="45e31-138">Затем Диспетчер TSF вызывает метод [иенумтфдисплайаттрибутеинфо:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) поставщика, добавляя каждый объект **итфдисплайаттрибутеинфо** , полученный в собственный перечислитель диспетчера, до тех пор, пока не будет достигнут конец перечисления поставщика.</span><span class="sxs-lookup"><span data-stu-id="45e31-138">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="45e31-139">Когда все объекты **итфдисплайаттрибутеинфо** для всех поставщиков отображаемых атрибутов добавляются в перечислитель диспетчера TSF, диспетчер возвращает его перечислитель клиенту.</span><span class="sxs-lookup"><span data-stu-id="45e31-139">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="45e31-140">Затем клиент вызывает метод **иенумтфдисплайаттрибутеинфо:: Next** один или несколько раз для получения объектов **итфдисплайаттрибутеинфо** .</span><span class="sxs-lookup"><span data-stu-id="45e31-140">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45e31-141">См. также</span><span class="sxs-lookup"><span data-stu-id="45e31-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e31-142">TF \_ дисплайаттрибуте</span><span class="sxs-lookup"><span data-stu-id="45e31-142">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="45e31-143">Итфкатегоримгр:: Регистеркатегори</span><span class="sxs-lookup"><span data-stu-id="45e31-143">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="45e31-144">итфдисплайаттрибутепровидер</span><span class="sxs-lookup"><span data-stu-id="45e31-144">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="45e31-145">иенумтфдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-145">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="45e31-146">Итфдисплайаттрибутепровидер:: Енумдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-146">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="45e31-147">итфдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-147">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="45e31-148">итфранже</span><span class="sxs-lookup"><span data-stu-id="45e31-148">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="45e31-149">итфпроперти</span><span class="sxs-lookup"><span data-stu-id="45e31-149">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="45e31-150">ITfContext:: Property</span><span class="sxs-lookup"><span data-stu-id="45e31-150">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="45e31-151">тфгуидатом</span><span class="sxs-lookup"><span data-stu-id="45e31-151">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="45e31-152">Итфкатегоримгр:: Регистергуид</span><span class="sxs-lookup"><span data-stu-id="45e31-152">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="45e31-153">Итфпроперти:: SetValue</span><span class="sxs-lookup"><span data-stu-id="45e31-153">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="45e31-154">Итфдисплайаттрибутемгр:: Жетдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-154">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="45e31-155">Итфдисплайаттрибутепровидер:: Жетдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-155">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="45e31-156">Итфдисплайаттрибутемгр:: Енумдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-156">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="45e31-157">иенумтфдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-157">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="45e31-158">Итфдисплайаттрибутепровидер:: Енумдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="45e31-158">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="45e31-159">Иенумтфдисплайаттрибутеинфо:: Next</span><span class="sxs-lookup"><span data-stu-id="45e31-159">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 





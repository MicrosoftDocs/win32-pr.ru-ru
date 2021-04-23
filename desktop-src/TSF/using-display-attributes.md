---
title: Использование атрибутов вывода
description: Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Платформа текстовых служб (TSF), атрибуты вывода
- TSF (платформа текстовых служб), атрибуты вывода
- Приложения с поддержкой TSF, атрибуты вывода
- атрибуты отображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773880"
---
# <a name="using-display-attributes"></a><span data-ttu-id="d45d6-107">Использование атрибутов вывода</span><span class="sxs-lookup"><span data-stu-id="d45d6-107">Using Display Attributes</span></span>

<span data-ttu-id="d45d6-108">Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста.</span><span class="sxs-lookup"><span data-stu-id="d45d6-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="d45d6-109">Это позволяет приложению отображать дополнительные визуальные отзывы.</span><span class="sxs-lookup"><span data-stu-id="d45d6-109">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="d45d6-110">Например, Текстовая служба проверки орфографии может выделить слово с ошибками с красной подчеркиванием.</span><span class="sxs-lookup"><span data-stu-id="d45d6-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="d45d6-111">Отображаемые атрибуты, которые могут быть предоставлены, определяются структурой [tf \_ дисплайаттрибуте](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) и включают цвет текста, цвет фона текста, стиль подчеркивания, цвет подчеркивания и толщину подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="d45d6-111">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="d45d6-112">При отрисовке текста приложение должно получать атрибуты отображения для текста, а атрибуты — изменять способ рисования текста.</span><span class="sxs-lookup"><span data-stu-id="d45d6-112">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="d45d6-113">Выполните следующие действия, чтобы получить атрибуты вывода.</span><span class="sxs-lookup"><span data-stu-id="d45d6-113">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="d45d6-114">Получите объект свойства для \_ атрибута Prop GUID \_ путем вызова [ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)GetObject.</span><span class="sxs-lookup"><span data-stu-id="d45d6-114">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="d45d6-115">Получите значение \_ атрибута Prop GUID \_ для указанного диапазона, вызвав метод [Итфреадонлипроперти:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span><span class="sxs-lookup"><span data-stu-id="d45d6-115">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="d45d6-116">Это предоставляет значение [тфгуидатом](tfguidatom.md) .</span><span class="sxs-lookup"><span data-stu-id="d45d6-116">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="d45d6-117">Преобразуйте значение [тфгуидатом](tfguidatom.md) в GUID, вызвав [итфкатегоримгр::](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span><span class="sxs-lookup"><span data-stu-id="d45d6-117">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="d45d6-118">Создайте объект [итфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) для атрибута дисплея, вызвав [Итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="d45d6-118">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="d45d6-119">Получите сведения об атрибутах вывода, вызвав [итфдисплайаттрибутеинфо:: жетаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="d45d6-119">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="d45d6-120">В следующем примере кода показана функция, которая получает отображаемые атрибуты из предоставленного контекста, Range и Edit cookie.</span><span class="sxs-lookup"><span data-stu-id="d45d6-120">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="d45d6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d45d6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d45d6-122">TF \_ дисплайаттрибуте</span><span class="sxs-lookup"><span data-stu-id="d45d6-122">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="d45d6-123">ITfContext:: Property</span><span class="sxs-lookup"><span data-stu-id="d45d6-123">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="d45d6-124">Итфреадонлипроперти:: GetValue</span><span class="sxs-lookup"><span data-stu-id="d45d6-124">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="d45d6-125">тфгуидатом</span><span class="sxs-lookup"><span data-stu-id="d45d6-125">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="d45d6-126">Итфкатегоримгр:: a GUID</span><span class="sxs-lookup"><span data-stu-id="d45d6-126">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="d45d6-127">итфдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="d45d6-127">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="d45d6-128">Итфдисплайаттрибутемгр:: Жетдисплайаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="d45d6-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="d45d6-129">Итфдисплайаттрибутеинфо:: Жетаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="d45d6-129">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 





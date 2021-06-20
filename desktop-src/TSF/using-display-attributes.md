---
title: Использование атрибутов вывода
description: Использование атрибутов отображения. Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Платформа текстовых служб (TSF), атрибуты вывода
- TSF (платформа текстовых служб), атрибуты вывода
- Приложения с поддержкой TSF, атрибуты вывода
- атрибуты отображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406137"
---
# <a name="using-display-attributes"></a>Использование атрибутов вывода

Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста. Это позволяет приложению отображать дополнительные визуальные отзывы. Например, Текстовая служба проверки орфографии может выделить слово с ошибками с красной подчеркиванием. Отображаемые атрибуты, которые могут быть предоставлены, определяются структурой [tf \_ дисплайаттрибуте](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) и включают цвет текста, цвет фона текста, стиль подчеркивания, цвет подчеркивания и толщину подчеркивания.

При отрисовке текста приложение должно получать атрибуты отображения для текста, а атрибуты — изменять способ рисования текста. Выполните следующие действия, чтобы получить атрибуты вывода.

1.  Получите объект свойства для \_ атрибута Prop GUID \_ путем вызова [ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)GetObject.
2.  Получите значение \_ атрибута Prop GUID \_ для указанного диапазона, вызвав метод [Итфреадонлипроперти:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue). Это предоставляет значение [тфгуидатом](tfguidatom.md) .
3.  Преобразуйте значение [тфгуидатом](tfguidatom.md) в GUID, вызвав [итфкатегоримгр::](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).
4.  Создайте объект [итфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) для атрибута дисплея, вызвав [Итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).
5.  Получите сведения об атрибутах вывода, вызвав [итфдисплайаттрибутеинфо:: жетаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).

В следующем примере кода показана функция, которая получает отображаемые атрибуты из предоставленного контекста, Range и Edit cookie.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[TF \_ дисплайаттрибуте](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext:: Property](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[Итфреадонлипроперти:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[тфгуидатом](tfguidatom.md)
</dt> <dt>

[Итфкатегоримгр:: a GUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[итфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[Итфдисплайаттрибутемгр:: Жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 Итфдисплайаттрибутеинфо:: Жетаттрибутеинфо 
</dt> </dl>

 

 





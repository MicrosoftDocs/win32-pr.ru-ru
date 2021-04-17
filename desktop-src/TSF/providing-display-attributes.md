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
# <a name="providing-display-attributes"></a>Предоставление атрибутов вывода

Платформа текстовых служб (TSF) позволяет текстовой службе предоставлять атрибуты для вывода текста. Это позволяет предоставить пользователю дополнительные визуальные отзывы. Например, Текстовая служба проверки орфографии может выделить слово с ошибками с красной подчеркиванием. Предоставленные атрибуты экрана определяются структурой [tf \_ дисплайаттрибуте](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) и включают цвет текста, цвет фона текста, стиль подчеркивания, цвет подчеркивания и толщину подчеркивания.

Клиенты, использующие эту информацию об атрибутах вывода, чаще всего являются приложениями, но могут также включать текстовые службы. Диспетчер TSF подводит между поставщиком атрибута дисплея и клиентом и отслеживает поставщик атрибута дисплея для конкретных атрибутов экрана.

Чтобы предоставить атрибуты вывода, служба текстового ввода должна выполнить следующие действия.

1.  Зарегистрируйте службу текста как поставщик атрибута просмотра, вызвав [итфкатегоримгр:: регистеркатегори](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) с идентификатором класса текстового сервиса для первого параметра, GUID \_ тфкат \_ дисплайаттрибутепровидер для второго параметра и идентификатор класса службы текстового ввода для третьего параметра.
2.  Реализуйте [итфдисплайаттрибутепровидер](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) и сделайте его доступным из фабрики классов.
3.  Реализуйте [иенумтфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) и сделайте его доступным из [Итфдисплайаттрибутепровидер:: енумдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).
4.  Реализуйте объект [итфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) для каждого типа отображаемого атрибута, предоставляемого службой текстового ввода.

## <a name="applying-the-display-attributes"></a>Применение атрибутов вывода

Текстовая служба должна применять атрибут дисплея к диапазону текста. Служба текстового ввода может изменять значение свойства только во время сеанса изменения, доступного для чтения и записи.

При условии, что это происходит в сеансе редактирования для чтения и записи, атрибут дисплея применяется следующим образом.

1.  Получите объект [итфранже](/windows/desktop/api/Msctf/nn-msctf-itfrange) , охватывающий текст, к которому будет применен атрибут вывода.
2.  Получите объект [итфпроперти](/windows/desktop/api/Msctf/nn-msctf-itfproperty) для текстовых атрибутов, вызвав [ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) GetObject с \_ атрибутом Prop GUID \_ .
3.  Создайте [тфгуидатом](tfguidatom.md) на основе определяемого службой текстового **интерфейса GUID** идентификатора атрибута, вызвав [итфкатегоримгр:: регистергуид](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).
4.  Инициализируйте переменную типа VARIANT для VT \_ I4 и задайте для элемента **Лвал** значение **тфгуидатом** , созданное на предыдущем шаге.
5.  Примените атрибут дисплея к диапазону, вызвав [итфпроперти:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) с файлом cookie для чтения и записи, диапазон и вариант, инициализированный на предыдущем шаге.


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



## <a name="supplying-the-display-attribute-information-object"></a>Предоставление объекта сведений о отображаемом атрибуте

Клиент получает объект **итфдисплайаттрибутеинфо** одним из двух способов.

1.  Клиент вызывает [итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) с идентификатором **GUID** атрибута дисплея. При первом вызове **итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо** диспетчер TSF создает экземпляр поставщика отображаемого атрибута, вызывая CoCreateInstance с идентификатором класса, переданным в качестве первого параметра в **Итфкатегоримгр:: регистеркатегори**. Последующие вызовы **итфдисплайаттрибутемгр:: жетдисплайаттрибутеинфо** будут использовать объект поставщика отображаемого атрибута.

    Затем Диспетчер TSF вызывает [итфдисплайаттрибутепровидер:: жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) с **идентификатором GUID** атрибута дисплея для получения объекта **итфдисплайаттрибутеинфо** .

    Затем Диспетчер TSF передает объект **итфдисплайаттрибутеинфо** обратно клиенту.

2.  Клиент вызывает [итфдисплайаттрибутемгр:: енумдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) , чтобы получить объект **иенумтфдисплайаттрибутеинфо** , содержащий все атрибуты вывода, предоставленные всеми поставщиками атрибутов просмотра. Диспетчер TSF перечисляет каждый поставщик атрибутов экрана и создает экземпляр каждого поставщика, вызывая CoCreateInstance с идентификатором класса, переданным в качестве третьего параметра в **итфкатегоримгр:: регистеркатегори**.

    Затем Диспетчер TSF вызывает **итфдисплайаттрибутепровидер:: енумдисплайаттрибутеинфо** каждого поставщика, чтобы получить объект **иенумтфдисплайаттрибутеинфо** , содержащий все атрибуты вывода, предоставленные поставщиком.

    Затем Диспетчер TSF вызывает метод [иенумтфдисплайаттрибутеинфо:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) поставщика, добавляя каждый объект **итфдисплайаттрибутеинфо** , полученный в собственный перечислитель диспетчера, до тех пор, пока не будет достигнут конец перечисления поставщика.

    Когда все объекты **итфдисплайаттрибутеинфо** для всех поставщиков отображаемых атрибутов добавляются в перечислитель диспетчера TSF, диспетчер возвращает его перечислитель клиенту. Затем клиент вызывает метод **иенумтфдисплайаттрибутеинфо:: Next** один или несколько раз для получения объектов **итфдисплайаттрибутеинфо** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[TF \_ дисплайаттрибуте](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[Итфкатегоримгр:: Регистеркатегори](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[итфдисплайаттрибутепровидер](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[иенумтфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[Итфдисплайаттрибутепровидер:: Енумдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[итфдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[итфранже](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[итфпроперти](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfContext:: Property](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[тфгуидатом](tfguidatom.md)
</dt> <dt>

[Итфкатегоримгр:: Регистергуид](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[Итфпроперти:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[Итфдисплайаттрибутемгр:: Жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[Итфдисплайаттрибутепровидер:: Жетдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[Итфдисплайаттрибутемгр:: Енумдисплайаттрибутеинфо](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 иенумтфдисплайаттрибутеинфо 
</dt> <dt>

 Итфдисплайаттрибутепровидер:: Енумдисплайаттрибутеинфо 
</dt> <dt>

[Иенумтфдисплайаттрибутеинфо:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 





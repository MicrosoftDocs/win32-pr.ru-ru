---
title: Свойства (общие элементы)
description: Платформа текстовых служб (TSF) предоставляет свойства, связывающие метаданные с диапазоном текста.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Платформа текстовых служб (TSF), свойства
- TSF (платформа текстовых служб), свойства
- текстовые службы, свойства
- Приложения, поддерживающие TSF, свойства
- properties
- Платформа текстовых служб (TSF), типы свойств
- TSF (платформа текстовых служб), типы свойств
- текстовые службы, типы свойств
- Приложения с поддержкой TSF, типы свойств
- типы свойств
- Платформа текстовых служб (TSF), постоянное хранение свойств
- TSF (платформа текстовых служб), постоянное хранение свойств
- текстовые службы, постоянное хранение свойств
- Приложения с поддержкой TSF, постоянное хранение свойств
- Постоянное хранение свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105681738"
---
# <a name="properties-common-elements"></a>Свойства (общие элементы)

Платформа текстовых служб (TSF) предоставляет свойства, связывающие метаданные с диапазоном текста. Эти свойства включают, но не ограничиваются, отображение таких атрибутов, как полужирный текст, идентификатор языка текста и необработанные данные, предоставляемые текстовыми службами, такими как звуковые данные, связанные с текстом из службы речевого текста.

В следующем примере показано, как можно просмотреть свойство гипотетического цвета текста с возможными значениями красного (R), зеленого (G) или синего цветов (B).


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Свойства различных типов могут перекрываться. Например, возьмем предыдущий пример и добавим текстовый атрибут, который может быть полужирным (B) или курсивом (I).


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Текст «this» будет полужирным, а ««» — полужирным и красным, «часть» будет отображаться обычным шрифтом, «цвет» будет зеленым и курсивом, а «текст» будет курсивом.

Свойства одного типа не могут перекрываться. Например, следующая ситуация недопустима, так как "-" и "Цветные" имеют перекрывающиеся значения одних и тех же типов.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Типы свойств

TSF определяет три различных типа свойств.



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Статические         | Объект статического свойства хранит данные свойства с текстом. Он также хранит диапазон текстовых данных для каждого диапазона, к которому применяется свойство. Итфреадонлипроперти:: GetType возвращает \_ \_ СТАТИЧЕСКУЮ категорию GUID тфкат пропстиле \_ .                                                                                                                                                                                                                      |
| Static-Compact | Объект свойства со статическим сжатием идентичен объекту статического свойства, за исключением того, что свойство со статическим сжатием не сохраняет данные диапазона. Когда запрашивается диапазон, охватываемый статическим свойством-Compact, для каждой группы смежных свойств создается диапазон. Статические свойства — это наиболее эффективный способ хранения свойств для отдельных символов. Итфреадонлипроперти:: GetType возвращает категорию GUID \_ тфкат \_ пропстиле \_ статиккомпакт. |
| Особые настройки         | Объект пользовательского свойства хранит сведения о диапазоне для каждого диапазона, к которому применяется свойство. Однако он не хранит фактические данные для свойства. Вместо этого в пользовательском свойстве хранится объект Итфпропертисторе. Диспетчер TSF использует этот объект для доступа к данным свойств и их обслуживания. Итфреадонлипроперти:: GetType возвращает GUID \_ тфкат \_ пропстиле \_ настраиваемую категорию.                                                                    |



 

## <a name="working-with-properties"></a>Работа со свойствами

Значения и атрибуты свойства получаются с помощью интерфейса [итфреадонлипроперти](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) и изменяются с помощью интерфейса [итфпроперти](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .

Если требуется указать конкретный тип свойства, используется [ITfContext::-Property](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) . Для **ITfContext::-Property** требуется **GUID** , определяющий получаемое свойство. TSF определяет набор [стандартных идентификаторов свойств](predefined-properties.md) , которые используются, или служба текстового ввода может определять собственные идентификаторы свойств. Если используется пользовательское свойство, поставщик свойств должен опубликовать **идентификатор GUID** свойства и формат полученных данных.

Например, чтобы получить **идентификатор CLSID** для владельца диапазона текста, вызовите метод **ITfContext::** GetObject, чтобы получить объект свойства, вызовите [итфпроперти:: финдранже](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) , чтобы получить диапазон, который полностью охватывает свойство, а затем вызовите метод [Итфреадонлипроперти:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) , чтобы получить [тфгуидатом](/windows/desktop/TSF/tfguidatom) , который представляет **идентификатор CLSID** службы текстового ввода, владеющей текстом. В следующем примере показана функция, которая задается контекстом, Range и Edit cookie, получит **идентификатор CLSID** службы текстового ввода, владеющей текстом.


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



Свойства также можно перечислить, получая интерфейс [иенумтфпропертиес](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) из [ITfContext:: енумпропертиес](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).

## <a name="persistent-storage-of-properties"></a>Постоянное хранение свойств

Часто свойства являются прозрачными для приложения и используются одной или несколькими текстовыми службами. Чтобы сохранить данные свойств, например, при сохранении в файл, приложение должно сериализовать данные свойства при сохранении и десериализации данных свойства при восстановлении данных. В этом случае приложению не следует заинтересовать отдельные свойства, но следует перечислить все свойства в контексте и сохранить их.

При хранении данных свойств приложение должно выполнить следующие действия.

1.  Получите перечислитель свойств путем вызова **ITfContext:: енумпропертиес**.
2.  Перечислите каждое свойство, вызвав метод [иенумтфпропертиес:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).
3.  Для каждого свойства получите перечислитель диапазона, вызвав [итфреадонлипроперти:: енумранжес](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).
4.  Перечислите каждый диапазон в свойстве, вызвав метод [иенумтфранжес:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).
5.  Для каждого диапазона в свойстве вызовите [итекстстореакпсервицес:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) со свойством, Range, структурой [ \_ \_ \_ \_ ACP постоянного свойства "TF PERSISTENT](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) " и объектом потока, реализованным приложением.
6.  Запишите содержимое структуры **\_ постоянного \_ \_ заголовка \_ Свойства "TF persistent** " в постоянную память.
7.  Запись содержимого объекта потока в постоянную память.
8.  Продолжайте предыдущие шаги для всех диапазонов во всех свойствах.
9.  Приложение должно записывать некоторый тип терминиатор в поток, чтобы при восстановлении данных можно было идентифицировать точку останова.


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



**Итекстстореакпсервицес:: сериализует**[Итфпропертисторе:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

При восстановлении данных свойств приложение должно выполнить следующие действия.

1.  Установите указатель потока на начало первой структуры **\_ постоянного \_ \_ заголовка \_ Свойства "TF PERSISTENT** ".
2.  Чтение структуры **\_ постоянного \_ \_ заголовка \_ Свойства "TF PERSISTENT** ".
3.  Вызовите **ITfContext:: Property** с элементом **гуидтипе** структуры **\_ \_ \_ \_ ACP постоянного свойства "TF PERSISTENT** ".
4.  На этом этапе приложение может выполнить одно из двух действий.
    1.  Создайте экземпляр объекта [итфперсистентпропертилоадеракп](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) , который должен быть реализован приложением. Затем вызовите [итекстстореакпсервицес:: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) со **значением NULL** для *пстреам* и указателем **итфперсистентпропертилоадеракп** .
    2.  Передайте входной поток в **итекстстореакпсервицес:: unserialize** и **null** для *плоадер*.

    Первый метод является предпочтительным, так как он наиболее эффективен. Реализация второго метода приводит к считыванию всех данных свойств из потока во время вызова **итекстстореакпсервицес:: unserialize** . Первый метод приводит к тому, что данные свойств будут считываться по запросу в более позднее время.
5.  Повторите предыдущие шаги, пока не будут десериализованы все блоки свойств.


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 

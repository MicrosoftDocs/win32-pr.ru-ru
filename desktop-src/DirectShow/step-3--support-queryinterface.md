---
description: предоставление клиентам новых интерфейсов фильтра в рамках создания страницы свойств фильтра для настраиваемого фильтра DirectShow.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Шаг 3. Поддержка QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0761a0ecf57bc7769cf40623c6929655a9f757b66b35bb506167d4263a7e02a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072458"
---
# <a name="step-3-support-queryinterface"></a>Шаг 3. Поддержка QueryInterface

Чтобы предоставить клиентам доступ к новым интерфейсам фильтра, выполните следующие действия.

-   Включите макрос [**Declare \_ IUnknown**](declare-iunknown.md) в раздел объявления Public фильтра:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Переопределите [**кункновн:: нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) , чтобы проверить наличие идентификаторов IID двух интерфейсов:
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

Далее. [Шаг 4. Создайте страницу свойств](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> <dt>

[Реализация IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




---
description: Шаг 3.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Шаг 3. Поддержка QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684286"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> <dt>

[Реализация IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




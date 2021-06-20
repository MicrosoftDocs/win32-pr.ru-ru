---
description: Реализуйте интерфейс ИспеЦифипропертипажес в фильтре в рамках создания страницы свойств фильтра для настраиваемого фильтра DirectShow.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Шаг 2. Реализация ИспеЦифипропертипажес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410057"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Шаг 2. Реализация ИспеЦифипропертипажес

Затем реализуйте интерфейс **испеЦифипропертипажес** в фильтре. Этот интерфейс содержит один метод, а **-страницы**, который ВОЗВРАЩАЕТ массив идентификаторов CLSID для страниц свойств, поддерживаемых фильтром. В этом примере фильтр содержит одну страницу свойств. Начните с создания идентификатора CLSID и объявления его в файле заголовка:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Теперь реализуйте **метод WebMethod** :


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Выделите память для массива с помощью функции **CoTaskMemAlloc**. Вызывающий объект выполнит освобождение памяти.

Далее. [Шаг 3. Поддержка QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 




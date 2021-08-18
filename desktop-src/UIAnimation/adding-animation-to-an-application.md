---
title: Создание основных объектов анимации
description: чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- объекты диспетчера анимации Windows анимация, создание
- объекты таймера анимации Windows анимация, создание
- объекты библиотеки переходов Windows анимация, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3023e5934581850bb6aa21e7d41d92642bb01fadfcf7531fcacabca74b411f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137407"
---
# <a name="create-the-main-animation-objects"></a>Создание основных объектов анимации

чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.

## <a name="overview"></a>Обзор

Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания диспетчера анимации, таймера анимации и объектов библиотеки переходов.

Эти объекты необходимы для создания и показа анимаций, поэтому они обычно не должны освобождаться до завершения работы приложения. Если ни один из зарегистрированных обратных вызовов не может создать ссылочный цикл, освобождение объектов достаточно для правильной очистки. В противном случае приложение может очищаться путем очистки обратных вызовов (передача **значений NULL** в месте каждого из них) или путем вызова метода [**завершения работы**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) диспетчера анимации.

## <a name="example-code"></a>Пример кода

следующий пример кода взят из файла MainWindow. cpp в примерах анимации Windows; см. метод Кмаинвиндов:: Инитиализеаниматион.


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



Обратите внимание на следующие определения из файла MainWindow. h.


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a>Следующий шаг

После завершения этого шага следующий шаг: [Создание переменных анимации](create-animation-variables.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**иуианиматионманажер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**иуианиматионтимер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**иуианиматионтранситионлибрари**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Windows Общие сведения об анимации](scenic-animation-api-overview.md)
</dt> </dl>

 

 
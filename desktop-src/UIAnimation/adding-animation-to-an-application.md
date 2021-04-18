---
title: Создание основных объектов анимации
description: Чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- Анимация объектов анимации Windows в объектах диспетчера анимации, создание
- Анимация объектов таймера Windows, создание
- Анимация объектов библиотек переходов Windows, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413432"
---
# <a name="create-the-main-animation-objects"></a>Создание основных объектов анимации

Чтобы использовать анимацию Windows в приложении, первым шагом является создание небольшого набора основных объектов анимации.

## <a name="overview"></a>Обзор

Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания диспетчера анимации, таймера анимации и объектов библиотеки переходов.

Эти объекты необходимы для создания и показа анимаций, поэтому они обычно не должны освобождаться до завершения работы приложения. Если ни один из зарегистрированных обратных вызовов не может создать ссылочный цикл, освобождение объектов достаточно для правильной очистки. В противном случае приложение может очищаться путем очистки обратных вызовов (передача **значений NULL** в месте каждого из них) или путем вызова метода [**завершения работы**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) диспетчера анимации.

## <a name="example-code"></a>Пример кода

Следующий пример кода взят из файла MainWindow. cpp в примерах анимации Windows. см. метод Кмаинвиндов:: Инитиализеаниматион.


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

## <a name="related-topics"></a>См. также

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**иуианиматионманажер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**иуианиматионтимер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**иуианиматионтранситионлибрари**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Общие сведения о анимации Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 
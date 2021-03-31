---
title: Повторное посещение правил агрегирования COM с помощью расширений ADSI
description: Ниже приведен краткий обзор правил агрегирования COM и расширения ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Расширения ADSI, правила объединения COM
- ADSI агрегирования COM
- Повторное посещение правил агрегирования COM с помощью расширений ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793843"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Повторное посещение правил агрегирования COM с помощью расширений ADSI

Ниже приведен краткий обзор правил агрегирования COM и расширения ADSI.

-   Метод **CreateInstance** возвращает указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , как показано ниже, который не делегирует вызовы функций в агрегатор.

    Метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Возвращает указатели на интерфейсы, которые он поддерживает, и ошибки для интерфейсов, которые он не поддерживает.

    Метод [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) увеличивает значение счетчика ссылок для объекта агрегированного расширения.

    Метод [**иунковн:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) уменьшает значение счетчика ссылок на объекте агрегированного расширения и удаляет себя, если счетчик ссылок равен 0.

-   В объекте расширения должен храниться указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) агрегатора, например m \_ паутерункновн, во время реализации метода **CreateInstance** .
-   Все интерфейсы, поддерживаемые объектом Extension, включая [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension), должны наследовать от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), который делегирует все вызовы функций обратно в агрегатор.
    -   [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) вызывает "m \_ Паутерункновн->QueryInterface"
    -   [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) вызывает "m \_ Паутерункновн->AddRef"
    -   [**Иунковн:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) вызывает "m \_ Паутерункновн->Release"

Модули записи расширений могут выбирать любую внутреннюю реализацию, если они подчиняются стандартным правилам агрегирования COM. Имейте в виду, что объект расширения не должен работать как автономный объект. Расширения предназначены для работы в виде статистических выражений. Однако расширение может быть написано для работы как как автономный объект, так и как агрегатная функция.

Помимо стандартной поддержки агрегирования COM, объект расширения может поддерживать [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) для более сложных функций. Если поддерживается позднее связывание, расширение должно:

-   Делегировать функции для [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) обратно в агрегатор.
-   Реализуйте интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 
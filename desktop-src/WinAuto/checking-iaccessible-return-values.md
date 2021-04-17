---
title: Проверка возвращаемых значений IAccessible
description: Разработчикам клиентов не следует полагаться на то, что макросы модели COM были УСПЕШНЫМи и не прошли проверку возвращаемых значений IAccessible, так как значения, отличные от S \_ ОК, считаются успешными.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710323"
---
# <a name="checking-iaccessible-return-values"></a>Проверка возвращаемых значений IAccessible

Разработчикам клиентов не следует полагаться на то, что макросы модели COM были [**успешными**](/windows/desktop/api/winerror/nf-winerror-succeeded) и [**не прошли**](/windows/desktop/api/winerror/nf-winerror-failed) проверку возвращаемых значений [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , так как значения, отличные от S \_ ОК, считаются успешными. Например, метод может возвращать \_ значение false, которое считается успешным при **успешном** выполнении макроса, но по-прежнему получил указатель **null** в выходном параметре.

Разработчики клиентов должны защищаться от вероятности возврата некоторыми серверами кодов ошибок, отличных от задокументированных значений. Для обеспечения безопасности необходимо убедиться, что все выходные параметры содержат действительные сведения и удовлетворяют следующим критериям.

-   Все указатели не **равны NULL**.
-   Элемент **VT** любой структуры [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) не равен VT \_ Empty.

 

 
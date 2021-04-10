---
title: Структура варианта
description: Большинство функций Active Accessibility Microsoft, а также свойств и методов IAccessible принимают в качестве параметра структуру VARIANT. По сути, структура VARIANT — это контейнер для большого объединения, который содержит много типов данных.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134103"
---
# <a name="variant-structure"></a>Структура варианта

Большинство функций Active Accessibility Microsoft, а также свойств и методов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) принимают в качестве параметра структуру [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . По сути, структура **Variant** — это контейнер для большого объединения, который содержит много типов данных.

Значение в первом члене структуры, **VT**, описывает, какое из членов Union является допустимым. Хотя структура [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) поддерживает множество различных типов данных, Microsoft Active Accessibility использует только следующие типы.



| Значение VT     | Имя соответствующего элемента значения |
|--------------|---------------------------------|
| VT \_ I4       | **лвал**                        |
| \_Диспетчер VT | **пдиспвал**                    |
| VT \_ BSTR     | **бстрвал**                     |
| VT \_ пуст    | нет                            |



 

При получении сведений в структуре [**варианта**](/windows/win32/api/oaidl/ns-oaidl-variant) Проверьте элемент **VT** , чтобы узнать, какой элемент содержит допустимые данные. Аналогично, при отправке данных с использованием структуры **Variant** всегда задавайте **VT** для отражения члена объединения, содержащего эти сведения.

Прежде чем использовать структуру, инициализируйте ее, вызвав функцию модели COM компонента [**вариантинит**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) . После завершения работы со структурой очистите ее, прежде чем память, содержащая [**вариант**](/windows/win32/api/oaidl/ns-oaidl-variant) , освобождается путем вызова [**вариантклеар**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 
---
title: Использование дочерних идентификаторов в параметрах
description: В этом разделе описываются входные параметры, выходные параметры и особые случаи для интерпретации дочерних идентификаторов, возвращаемых методами IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03026e6abf769efab95cc513231fad3af64511f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413209"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Использование дочерних идентификаторов в параметрах

В этом разделе описываются входные параметры, выходные параметры и особые случаи для интерпретации дочерних идентификаторов, возвращаемых методами [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="input-parameters"></a>Входные параметры

Многие функции Microsoft Active Accessibility и большинство свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) принимают [**вариантную**](/windows/win32/api/oaidl/ns-oaidl-variant) структуру в качестве входного параметра. Для большинства свойств **IAccessible** этот параметр позволяет разработчикам клиентов указать, требуется ли пользователю получить сведения о самом объекте или об одном из простых элементов объекта.

Microsoft Active Accessibility предоставляет постоянную **чилдид \_** , которая указывает, что информация необходима для самого объекта. Чтобы получить сведения о простом элементе, разработчики клиента указывают свой дочерний идентификатор в параметре [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

При инициализации параметра [**типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) не забудьте указать **VT \_ I4** в элементе **VT** , а также указать значение идентификатора дочернего элемента (или **чилдид \_ Self**) в элементе **лвал** .

Например, чтобы получить имя объекта, а не один из дочерних элементов объекта, инициализируйте [**вариант**](/windows/win32/api/oaidl/ns-oaidl-variant) первого параметра метода [**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **Чилдид \_ Self** в элементе **лвал** и **VT \_ I4** в элементе **VT** ), а затем вызовите метод **IAccessible:: Get \_ аккнаме**.

## <a name="output-parameters"></a>Выходные параметры

Несколько функций и методов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) имеют [](/windows/win32/api/oaidl/ns-oaidl-variant) \* выходной параметр Variant, который содержит идентификатор дочернего объекта или указатель интерфейса [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) на дочерний объект. Клиент должен выполнить различные действия в зависимости от того, получал ли он дочерний идентификатор объекта **VT \_** (простой элемент) или указатель интерфейса **IDispatch** с **чилдид \_ Self** (полный объект). После выполнения этих действий будет предоставлен указатель интерфейса **IAccessible** и идентификатор дочернего элемента, которые позволяют клиентам использовать методы и свойства **IAccessible** . Эти действия относятся к методам [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**Get \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)и [**Get \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) . Они также применяются к клиентским функциям [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)и [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

В следующей таблице перечислены возможные возвращаемые результаты и необходимые действия, выполняемые после обработки, чтобы клиенты имели указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатор дочернего элемента.



| Возвращенный результат                                      | После обработки возвращаемого значения                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Указатель интерфейса [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Это полный объект. Вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для доступа к указателю интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Используйте указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) с **чилдид \_ Self** для доступа к методам и свойствам **IAccessible** .<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_Идентификатор дочернего элемента VT I4                                      | Вызовите метод [**IAccessible:: Get \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) , используя идентификатор дочернего элемента, чтобы проверить, есть ли у вас указатель интерфейса [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . Если вы получаете указатель интерфейса [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , используйте его с **чилдид \_ Self** для доступа к методам и свойствам интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Если вызов [**Get \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) завершается неудачей, у вас есть простой элемент. Используйте исходный указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (тот, который использовался при вызове метода или функции, упомянутой выше) с идентификатором дочернего элемента **VT \_ I4** , возвращенным вызовом.<br/> |



 

Прежде чем можно будет использовать параметр [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , его необходимо инициализировать, вызвав функцию модели COM компонента [**вариантинит**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) . После завершения работы со структурой вызовите [**вариантклеар**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) , чтобы освободить память, зарезервированную для этого **варианта**.

## <a name="special-cases"></a>Особые случаи

Существуют исключения из правил, приведенных в таблице выше, например, когда идентификатор дочернего элемента возвращается методом [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) . Серверы должны возвращать интерфейс [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , если дочерний объект является доступным объектом. Если в **IAccessible:: акчиттест** возвращается дочерний идентификатор, то дочерний элемент является простым.

Кроме того, существуют особые случаи для [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Дополнительные сведения см. в разделе **IAccessible:: аккнавигате** , [пространственные и логическая Навигация](spatial-and-logical-navigation.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Интерфейс IDispatch](idispatch-interface.md)
</dt> <dt>

[Структура варианта](variant-structure.md)
</dt> </dl>

 


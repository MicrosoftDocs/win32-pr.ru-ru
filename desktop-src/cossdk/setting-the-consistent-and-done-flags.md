---
description: Установка флагов consistent и Done
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Установка флагов consistent и Done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518864efda3716ea9998ed306b0ca6901b70697f8cb3acabe813d3e2e3e0bcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500054"
---
# <a name="setting-the-consistent-and-done-flags"></a>Установка флагов consistent и Done

Флаги consistent и Done задаются путем вызова методов для интерфейсов [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) или [**иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) . Стратегии, используемые этими двумя интерфейсами, значительно отличаются. **Иобжектконтекст** имеет четыре метода, которые привязывают последовательные и выполненные флаги вместе в уникальных сочетаниях, в то время как **иконтекстстате** имеет два метода, позволяющих устанавливать каждый флаг независимо друг от друга. Методы **иобжектконтекст** также предоставляются через объект [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Для независимого управления каждым флагом [**иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) предоставляет метод для установки флага Consistent в значение true или false и метод для установки флага done в значение true или false. Эти методы являются [**сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) и [**сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn)соответственно. Интерфейс **иконтекстстате** также включает методы для получения текущего значения каждого флага.

При задании значения Ткскоммит для метода [**СЕТМИТРАНСАКТИОНВОТЕ**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) com+ проверяет наличие транзакции. Если COM+ не обнаруживает транзакцию, выдается ошибка, которую можно записать в файл журнала. Например, предположим, что кто-то случайно настраивает атрибут транзакции компонента в неподдерживаемом виде, но ожидалось, что он должен быть установлен в значение обязательное. Установив **сетмитрансактионвоте** = ткскоммит, можно задать конфликт и выполнить действие.

В следующей таблице описаны вызовы методов, которые можно использовать для установки флагов consistent и Done.



| Флаг соответствия  | Флаг "Готово"        | Метод Иобжектконтекст                                            | Методы Иконтекстстате                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Верно<br/>  | Нет<br/> | [**енаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте* = ткскоммит <br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате* = false<br/> |
| Неверно<br/> | False<br/> | [**дисаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте* = тксаборт <br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате* = false<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте* = тксаборт <br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате* = true<br/>   |
| True<br/>  | True<br/>  | [**сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте* = ткскоммит <br/>[**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате* = true              |



 

> [!Note]  
> Свойство автозаполнения, заданное на уровне метода, может влиять на то, как устанавливаются флаги consistent и Done. Дополнительные сведения о свойстве автоматического завершения см. в разделе [Включение автозаполнения для метода](enabling-auto-done-for-a-method.md) и [Установка бита done](setting-the-done-bit.md).

 

 

 





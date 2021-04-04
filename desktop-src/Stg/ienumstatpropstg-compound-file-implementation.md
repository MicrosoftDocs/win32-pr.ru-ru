---
title: Реализация файла IEnumSTATPROPSTG-Compound
description: Реализация составного файла интерфейса Иенумстатпропстг используется для перечисления свойств, в результате чего структуры СТАТПРОПСТГ, которые содержат данные статистических свойств.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- Иенумстатпропстг Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987784"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>Реализация файла IEnumSTATPROPSTG-Compound

Реализация составного файла интерфейса [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) используется для перечисления свойств, в результате чего структуры [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , которые содержат данные статистических свойств. Реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) управляет статистическими данными и связывается с текущим объектом хранилища составного файла.

Конструктор в реализации COM [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) создает класс, который считывает набор свойств и создает статический массив, который может использоваться совместно при вызове **Иенумстатпропстг:: Clone** .

## <a name="when-to-use"></a>Назначение

Вызовите реализацию составного файла [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , чтобы перечислить структуры [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , содержащие данные о свойствах в текущем наборе свойств. При использовании реализации составного файла интерфейсов хранилища свойств вызовите [**ипропертистораже:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) , чтобы вернуть указатель на **иенумстатпропстг** для управления объектом хранилища свойств и элементами внутри него.

## <a name="remarks"></a>Комментарии

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**Иенумстатпропстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Возвращает следующую одну или несколько структур [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (число определяется параметром *celt* ). \_При успешном выполнении возвращает значение ОК.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**Иенумстатпропстг:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Пропускает количество элементов, указанное в параметре *celt*. Следующий элемент, который будет перечисляться с помощью вызова Next, станет элементом после пропущенных элементов. Возвращает \_ значение "ОК", если значения *celt* пропущены; \_ Если пропущено менее *celt* элементов, возвращает s false.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**Иенумстатпропстг:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Устанавливает курсор в начало перечисления. В случае успеха возвращает S \_ ОК, в противном случае ВОЗВРАЩАЕТ STG \_ E \_ инвалидхандле.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**Иенумстатпропстг:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Использует конструктор для [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , чтобы создать копию массива. Поскольку класс, создающий статический массив, фактически содержит объект, эта функция в основном добавляет к счетчику ссылок.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**Ипропертистораже:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 
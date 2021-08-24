---
description: Таблица ComPlus содержит сведения, необходимые для установки приложений COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Таблица ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77885688226689e5d81e074b1a9a28ef3801aaeba5febf51165377ac9ad9e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144975"
---
# <a name="complus-table"></a>Таблица ComPlus

Таблица ComPlus содержит сведения, необходимые для установки приложений COM+.

Таблица ComPlus содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Компонент\_ | [Идентификатор](identifier.md) | Д   | Нет        |
| експтипе     | [Integer](integer.md)       | Нет   | Д        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в первом столбце [таблицы Component](component-table.md). Это компонент, содержащий приложение COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>експтипе
</dt> <dd>

Флаги экспорта, используемые при создании файла .msi. дополнительные сведения см. в документации по COM+ в пакете Microsoft Windows Software Development Kit (SDK).

</dd> </dl>

## <a name="remarks"></a>Remarks

См. действие [регистеркомплус](registercomplus-action.md) и [действие унрегистеркомплус](unregistercomplus-action.md).

см. раздел [установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 




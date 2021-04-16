---
description: Таблица ComPlus содержит сведения, необходимые для установки приложений COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Таблица ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651138"
---
# <a name="complus-table"></a>Таблица ComPlus

Таблица ComPlus содержит сведения, необходимые для установки приложений COM+.

Таблица ComPlus содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Компонент\_ | [Идентификатор](identifier.md) | Да   | Нет        |
| експтипе     | [Integer](integer.md)       | Нет   | Да        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в первом столбце [таблицы Component](component-table.md). Это компонент, содержащий приложение COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>експтипе
</dt> <dd>

Флаги экспорта, используемые при создании MSI файла. Дополнительные сведения см. в документации по COM+ в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.

</dd> </dl>

## <a name="remarks"></a>Комментарии

См. действие [регистеркомплус](registercomplus-action.md) и [действие унрегистеркомплус](unregistercomplus-action.md).

См. раздел [Установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 




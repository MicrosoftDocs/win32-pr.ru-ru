---
description: ICE73 проверяет, что пакет не использует коды пакетов, коды обновления или коды продуктов установщик Windows примеров пакета SDK. Пакеты никогда не должны повторно использовать коды пакета, обновления или продукта другого продукта.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662589"
---
# <a name="ice73"></a>ICE73

ICE73 проверяет, что пакет не использует коды пакетов, коды обновления или коды продуктов установщик Windows примеров пакета SDK. Пакеты никогда не должны повторно использовать коды пакета, обновления или продукта другого продукта.

## <a name="result"></a>Результат

ICE73 выводит предупреждение, если пакет продукта повторно использует код пакета или продукта в образце пакета SDK установщик Windows.

## <a name="example"></a>Пример

ICE73 сообщает о следующих ошибках в приведенном примере:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Звездочки ( \* \* \* \* ) в GUID представляют диапазон идентификаторов GUID, зарезервированных для последующих пакетов SDK установщик Windows.

 

Чтобы устранить ошибки, создайте уникальный идентификатор GUID для продукта пакета и кодов пакетов. Кроме того, вам потребуется новый уникальный идентификатор GUID для кода обновления пакета.

[Поток сводных данных](summary-information-stream.md) (частичный)



| Свойство       | Значение                                  |
|----------------|----------------------------------------|
| Идентификатор процесса \_ ревнумбер | {000C1101-0000-0000-C000-000000000047} |



 

[Таблица свойств](property-table.md) (частичная)



| Свойство                           | Значение                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**UpgradeCode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Коды пакетов](package-codes.md)
</dt> <dt>

[Коды продуктов](product-codes.md)
</dt> <dt>

[**Свойство сводки номеров редакций**](revision-number-summary.md)
</dt> <dt>

[**UpgradeCode, свойство**](upgradecode.md)
</dt> <dt>

[**ProductCode, свойство**](productcode.md)
</dt> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 




---
description: ICE73 проверяет, что пакет не использует коды пакетов, коды обновления или коды продуктов установщик Windows примеров пакета SDK. Пакеты никогда не должны повторно использовать коды пакета, обновления или продукта другого продукта.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e5beecbfc7b4345d3b0dd7a93b86c55acc1abde4cc4f99d72749368be9d303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635080"
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
> звездочки ( \* \* \* \* ) в GUID представляют диапазон идентификаторов guid, зарезервированных для последующих пакетов SDK установщик Windows.

 

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



 

## <a name="related-topics"></a>Связанные темы

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

 

 




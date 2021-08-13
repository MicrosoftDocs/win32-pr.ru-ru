---
description: Действие RegisterUser регистрирует сведения о пользователе с помощью установщика для обнаружения пользователя продукта.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Действие RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626719"
---
# <a name="registeruser-action"></a>Действие RegisterUser

Действие RegisterUser регистрирует сведения о пользователе с помощью установщика для обнаружения пользователя продукта.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Ограничения последовательности отсутствуют.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия   |
|-------|------------------------------|
| \[1\] | Зарегистрированные сведения о пользователе. |



 

## <a name="remarks"></a>Remarks

Действие RegisterUser не выполняется во время административной установки. Если идентификатор продукта, введенный пользователем, не был проверен [действием валидатепродуктид](validateproductid-action.md), свойство [**ProductID**](productid.md) не задается и это действие не выполняет никаких действий.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ИМЕН**](username.md)
</dt> <dt>

[**Название**](companyname.md)
</dt> <dt>

[**Кодом**](productid.md)
</dt> </dl>

 

 




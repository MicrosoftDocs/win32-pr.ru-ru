---
description: Действие RegisterUser регистрирует сведения о пользователе с помощью установщика для обнаружения пользователя продукта.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Действие RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813641"
---
# <a name="registeruser-action"></a>Действие RegisterUser

Действие RegisterUser регистрирует сведения о пользователе с помощью установщика для обнаружения пользователя продукта.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Ограничения последовательности отсутствуют.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия   |
|-------|------------------------------|
| \[1\] | Зарегистрированные сведения о пользователе. |



 

## <a name="remarks"></a>Комментарии

Действие RegisterUser не выполняется во время административной установки. Если идентификатор продукта, введенный пользователем, не был проверен [действием валидатепродуктид](validateproductid-action.md), свойство [**ProductID**](productid.md) не задается и это действие не выполняет никаких действий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ИМЕН**](username.md)
</dt> <dt>

[**Название**](companyname.md)
</dt> <dt>

[**Кодом**](productid.md)
</dt> </dl>

 

 




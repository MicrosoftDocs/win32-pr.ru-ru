---
description: 'Существуют три функции, которые создают диалоговые окна для управления ошибками: Сетупкоперрор, Сетупделетиррор и Сетупренамиррор.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Обработка ошибок (API установки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662553"
---
# <a name="error-handling-setup-api"></a>Обработка ошибок (API установки)

Существуют три функции, которые создают диалоговые окна для управления ошибками: [**сетупкоперрор**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**сетупделетиррор**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)и [**сетупренамиррор**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

Подпрограммы обратного вызова могут использовать эти функции для создания пользовательского интерфейса для управления уведомлениями [**спфиленотифи \_ коперрор**](spfilenotify-copyerror.md), [**спфиленотифи \_ делетиррор**](spfilenotify-deleteerror.md)и [**спфиленотифи \_ ренамиррор**](spfilenotify-renameerror.md) .

Каждая из этих функций обработки ошибок создает диалоговое окно, предлагающее пользователю получить сведения о том, как продолжать работу. Как и в случае с [**сетуппромптфордиск**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), можно изменить макет и поведение диалогового окна, указав флаги во время вызова функции.

 

 




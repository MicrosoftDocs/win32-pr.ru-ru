---
description: Векторные обработчики исключений являются расширением для структурированной обработки исключений.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Обработка векторных исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926b0499e9399aa77e6835e90c6da016da3f2dc8195a4b4872f7f5119d04978a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405585"
---
# <a name="vectored-exception-handling"></a>Обработка векторных исключений

Векторные обработчики исключений являются расширением для структурированной обработки исключений. Приложение может зарегистрировать функцию для просмотра или обработки всех исключений приложения. Векторные обработчики не основаны на кадрах, поэтому можно добавить обработчик, который будет вызываться независимо от того, где находится в кадре вызова. Векторные обработчики вызываются в том порядке, в котором они были добавлены, когда отладчик получает первое уведомление о шансе, но до того, как система начнет раскрутить стек.

Чтобы добавить векторный обработчик Continue, используйте функцию [**аддвекторедконтинуехандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) . Чтобы удалить этот обработчик, используйте функцию [**ремовевекторедконтинуехандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .

Чтобы добавить векторный обработчик исключений, используйте функцию [**аддвекторедексцептионхандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) . Чтобы удалить этот обработчик, используйте функцию [**ремовевекторедексцептионхандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .

 

 

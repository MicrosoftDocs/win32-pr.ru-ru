---
title: Функции (сенсорный ввод Windows)
description: Этот раздел содержит функции для сенсорного ввода Windows.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Касание Windows, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071034"
---
# <a name="functions-windows-touch-input"></a>Функции (сенсорный ввод Windows)

Этот раздел содержит функции для сенсорного ввода Windows.

Для сенсорного ввода Windows используются следующие функции.



| Функция                                                                                               | Описание                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**клосетаучинпусандле**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | Закрывает входной маркер касания, освобождает память процесса, связанную с ним, и делает этот маркер недействительным.                                       |
| [**жеттаучинпутинфо**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | Получает подробные сведения о сенсорных вводах, связанных с конкретным сенсорным входом.                                        |
| [**истаучвиндов**](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | Проверяет, поддерживает ли указанное окно сенсорное касание, и, при необходимости, получает флаги модификаторов, заданные для функции касания окна. |
| [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | Регистрирует окно с поддержкой сенсорного ввода.                                                                                              |
| [**унрегистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | Регистрирует окно, так как оно больше не поддерживает сенсорный ввод.                                                                                    |
| [SendMessage, сообщение и связанные функции](sendmessage--postmessage--and-related-functions.md) | Содержит рекомендации по пересылке сообщений.                                                                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сенсорный ввод Windows](multi-touch-input.md)
</dt> <dt>

[Справочное руководством по программированию ввода Windows Touch](guide-multi-touch-input.md)
</dt> </dl>

 

 





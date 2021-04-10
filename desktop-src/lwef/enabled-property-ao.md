---
title: Свойство Enabled (объект Аудиуутпут)
description: Свойство Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071022"
---
# <a name="enabled-property-audiooutput-object"></a>Свойство Enabled (объект Аудиуутпут)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает логическое значение, указывающее, включены ли выходные данные звука (речь).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*агент * * *. Аудиуутпут. Enabled**



| Значение     | Описание                               |
|-----------|-------------------------------------------|
| **True**  | Параметры Включен речевой вывод. |
| **False** | Речевое Выходное звуковое сопровождение отключено.          |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это свойство отражает параметр воспроизведение аудио вывода на странице вывод страницы свойств агента (дополнительные параметры символов). Если свойство [**Enabled**](enabled-property.md) возвращает **значение true**, то метод [**говорите**](speak-method.md) создает выходные данные, если установлен совместимый обработчик TTS, или для речевого вывода используются звуковые файлы. При возврате значения **false** это означает, что речевой вывод не установлен или отключен пользователем. Параметр свойства применяется ко всем символам агента и доступен только для чтения; только пользователь может установить это значение свойства.

## <a name="see-also"></a>См. также:

[Событие Ажентпропертичанже](agentpropertychange-event.md)


 

 





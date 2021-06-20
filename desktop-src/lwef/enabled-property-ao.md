---
title: Свойство Enabled (объект Аудиуутпут)
description: Сведения о включенном свойстве объекта Аудиуутпут. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407347"
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

## <a name="remarks"></a>Remarks

Это свойство отражает параметр воспроизведение аудио вывода на странице вывод страницы свойств агента (дополнительные параметры символов). Если свойство [**Enabled**](enabled-property.md) возвращает **значение true**, то метод [**говорите**](speak-method.md) создает выходные данные, если установлен совместимый обработчик TTS, или для речевого вывода используются звуковые файлы. При возврате значения **false** это означает, что речевой вывод не установлен или отключен пользователем. Параметр свойства применяется ко всем символам агента и доступен только для чтения; только пользователь может установить это значение свойства.

## <a name="see-also"></a>См. также

[Событие Ажентпропертичанже](agentpropertychange-event.md)


 

 





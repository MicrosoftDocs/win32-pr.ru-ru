---
title: Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается
description: Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443153"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложений Магазина Windows не поддерживается

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8,1  
Серверы — Windows Server 2012 R2  
</dl>

## <a name="description"></a>Описание

Вызов Иммсетконверсионстатус () или Иммжетконверсионстатус () из приложения Магазина Windows не поддерживается и может привести к непредвиденным результатам.

## <a name="manifestations"></a>Проявлениями

При запуске приложения в режиме IME задаются следующие значения по умолчанию:



| &nbsp;   | Панель программного ввода | Аппаратная клавиатура |
|----------|----------------------|-------------------|
| KOR, JPN | С                   | Выкл.               |
| CHS, CHT | Включено                   | Включено                |



 

## <a name="solution"></a>Решение

Разработчики могут управлять режимом IME по умолчанию, указывая значение области ввода для поля.

Режим IME для заданной области ввода определяется каждым IME. Разработчики не могут указать режим IME.

## <a name="resources"></a>Ресурсы

-   [Перечисление Инпутскопе](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [иммсетконверсионстатус](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [иммжетконверсионстатус](/previous-versions/aa912903(v=msdn.10))

 

 
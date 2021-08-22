---
title: вызов иммсетконверсионстатус () или иммжетконверсионстатус () из приложений магазина Windows не поддерживается
description: вызов иммсетконверсионстатус () или иммжетконверсионстатус () из приложений магазина Windows не поддерживается
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9950bc008ce96d6c0a80a6090c3312057a12c4a7a1f64a5563625a518831c27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348574"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>вызов иммсетконверсионстатус () или иммжетконверсионстатус () из приложений магазина Windows не поддерживается

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8,1  
серверы — Windows Server 2012 R2  
</dl>

## <a name="description"></a>Описание

вызов иммсетконверсионстатус () или иммжетконверсионстатус () из приложения магазина Windows не поддерживается и может привести к непредвиденным результатам.

## <a name="manifestations"></a>Проявлениями

При запуске приложения в режиме IME задаются следующие значения по умолчанию:



| &nbsp;   | Панель программного ввода | Аппаратная клавиатура |
|----------|----------------------|-------------------|
| KOR, JPN | Включен                   | Off               |
| CHS, CHT | Включено                   | Включено                |



 

## <a name="solution"></a>Решение

Разработчики могут управлять режимом IME по умолчанию, указывая значение области ввода для поля.

Режим IME для заданной области ввода определяется каждым IME. Разработчики не могут указать режим IME.

## <a name="resources"></a>Ресурсы

-   [Перечисление Инпутскопе](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [иммсетконверсионстатус](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [иммжетконверсионстатус](/previous-versions/aa912903(v=msdn.10))

 

 
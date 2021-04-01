---
title: Структура WinSNMP
description: Функции WinSNMP API используют следующие структуры.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP-структуры SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890840"
---
# <a name="winsnmp-structures"></a>Структура WinSNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Функции WinSNMP API используют следующие структуры.



| Структура                                  | Описание                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Содержит 64-битовое целочисленное значение без знака, представляющее счетчик.                                                    |
| [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Содержит указатель на строку октета SNMP с переменной длиной.                                                         |
| [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Содержит указатель на массив переменной длины субидентификаторов, связанных с указанным именованным объектом. |
| [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Представляет значение, связанное с именем переменной в записи привязки переменной.                              |
| [**смивендоринфо**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Содержит сведения о реализации WinSNMP в Майкрософт.                                                    |



 

 

 
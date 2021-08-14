---
description: Допустимый функциональный дескриптор безопасности содержит сведения о безопасности в двоичном формате.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Строки дескрипторов безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413794"
---
# <a name="security-descriptor-strings"></a>Строки дескрипторов безопасности

Допустимый функциональный [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) содержит сведения о безопасности в двоичном формате. Windows API предоставляет функции для преобразования двоичных дескрипторов безопасности в текстовые строки и из них. Дескрипторы безопасности в строковом формате не работают, но они могут быть полезны для хранения или переноса сведений о дескрипторах безопасности.

Чтобы преобразовать дескриптор безопасности в строковый формат, вызовите функцию [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) . Чтобы преобразовать дескриптор безопасности строкового формата обратно в допустимый функциональный дескриптор безопасности, вызовите функцию [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .

Дополнительные сведения см. в разделе [язык определения дескрипторов безопасности](security-descriptor-definition-language.md).

 

 

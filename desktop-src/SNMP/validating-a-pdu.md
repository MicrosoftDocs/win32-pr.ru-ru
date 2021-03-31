---
title: Проверка PDU
description: Если приложение WinSNMP вызывает функцию Снмпсендмсг или Снмпенкодемсг, то реализация Microsoft WinSNMP проверяет допустимость PDU и другие параметры функции.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411228"
---
# <a name="validating-a-pdu"></a>Проверка PDU

Если приложение WinSNMP вызывает функцию [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) или [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , то реализация Microsoft WINSNMP проверяет допустимость PDU и другие параметры функции.

Значение одного компонента данных PDU (или поля) может быть допустимым по отдельности, но оно может быть недопустимым в сочетании со значениями других полей. Например, если в качестве значения поля **\_ типа PDU** для PDU используется SNMP- \_ PDU \_ или \_ \_ отклика PDU SNMP, то оба поля **\_ состояния ошибки** и **\_ индекса ошибки** должны быть равны нулю. Любое другое сочетание значений представляет собой недопустимый PDU.

Реализация отклоняет недопустимые PDU и возвращает состояние ошибки СНМПАПИ \_ сбой. Он устанавливает расширенный код ошибки, равный СНМПАПИ \_ PDU \_ .

 

 





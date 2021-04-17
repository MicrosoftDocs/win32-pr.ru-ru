---
title: Credential Guard и сторонние приложения
description: Credential Guard не позволяет сторонним поставщикам общих служб запрашивать хэш-коды паролей из LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487732"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Сторонние поставщики поддержки безопасности с Credential Guard

Credential Guard не позволяет сторонним поставщикам общих служб запрашивать хэш-коды паролей из LSA. При этом SSP и AP все равно получают уведомление о пароле, когда пользователь входит в систему или меняет пароль. Никакое использование недокументированных API с другими поставщиками общих служб и AP не поддерживается.

По мере увеличения масштабов защиты, осуществляемой Credential Guard, последующие выпуски Windows 10 с работающим Credential Guard могут повлиять на сценарии, которые работали в прошлом. Например, Credential Guard может заблокировать использование определенного типа учетных данных или определенного компонента, чтобы не позволить вредоносному ПО воспользоваться уязвимостями. Поэтому мы рекомендуем проверять сценарии, необходимые для работы организации, перед обновлением устройств с работающим Credential Guard.

Полное описание и рекомендуемые способы устранения этой проблемы см. в [этой статье](/windows/security/identity-protection/credential-guard/credential-guard) .

 

 
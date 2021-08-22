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
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706754"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Сторонние поставщики поддержки безопасности с Credential Guard

Credential Guard не позволяет сторонним поставщикам общих служб запрашивать хэш-коды паролей из LSA. При этом SSP и AP все равно получают уведомление о пароле, когда пользователь входит в систему или меняет пароль. Никакое использование недокументированных API с другими поставщиками общих служб и AP не поддерживается.

По мере увеличения масштабов защиты, осуществляемой Credential Guard, последующие выпуски Windows 10 с работающим Credential Guard могут повлиять на сценарии, которые работали в прошлом. Например, Credential Guard может заблокировать использование определенного типа учетных данных или определенного компонента, чтобы не позволить вредоносному ПО воспользоваться уязвимостями. Поэтому мы рекомендуем проверять сценарии, необходимые для работы организации, перед обновлением устройств с работающим Credential Guard.

Полное описание и рекомендуемые способы устранения этой проблемы см. в [этой статье](/windows/security/identity-protection/credential-guard/credential-guard) .

 

 
---
description: Задает или получает логическое значение, указывающее, можно ли использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Свойство Settings. Енаблепромптфорцертификатеуи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688962"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Свойство Settings. Енаблепромптфорцертификатеуи

\[Свойство **енаблепромптфорцертификатеуи** доступно для использования в операционных системах, указанных в разделе требования.\]

Свойство **енаблепромптфорцертификатеуи** задает или получает логическое значение, указывающее, можно ли использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя.

## <a name="syntax"></a>Синтаксис


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Значение свойства

Если **значение — true**, можно использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя. Значение по умолчанию — **false**.

> [!Note]  
> Задание этого свойства не отключает предупреждения, которые генерируются до того, как использование закрытого ключа выполняется из веб-приложения.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Параметры**](settings.md)
</dt> </dl>

 

 





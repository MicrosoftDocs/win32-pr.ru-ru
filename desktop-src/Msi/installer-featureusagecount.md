---
description: Свойство Феатуреусажекаунт — это свойство, доступное только для чтения и возвращающее количество раз, когда была использована функция.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Свойство Installer. Феатуреусажекаунт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f0f8444909d07655949cd35d060eb455e5a153fc2b897e757c2fdde2d1d731d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631203"
---
# <a name="installerfeatureusagecount-property"></a>Свойство Installer. Феатуреусажекаунт

Свойство **феатуреусажекаунт** — это свойство, доступное только для чтения и возвращающее количество раз, когда была использована функция.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Использование методов [**усефеатуре**](installer-usefeature.md), [**провидекомпонент**](installer-providecomponent.md) или [**ПРОВИДЕКУАЛИФИЕДКОМПОНЕНТ**](installer-providequalifiedcomponent.md) или их эквивалентов API для указанного компонента увеличивает это свойство.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсижетфеатуреусаже**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 





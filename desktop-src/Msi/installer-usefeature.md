---
description: Метод Усефеатуре объекта Installer увеличивает счетчик использования для определенной функции и возвращает состояние установки для этой функции. Этот метод следует использовать для указания намерения приложения использовать функцию.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Метод Installer. Усефеатуре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b320ce72271bb7ee90ac85a376b103d868e6f740a2e853daf58bb478dc79ad6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142160"
---
# <a name="installerusefeature-method"></a>Метод Installer. Усефеатуре

Метод **усефеатуре** объекта [**Installer**](installer-object.md) увеличивает счетчик использования для определенной функции и возвращает состояние установки для этой функции. Этот метод следует использовать для указания намерения приложения использовать функцию.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Продукт* 
</dt> <dd>

Указывает код продукта.

</dd> <dt>

*Компонент* 
</dt> <dd>

Определяет используемую функцию.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Этот параметр должен быть *мсиинсталлмоденодетектион*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод **усефеатуре** следует использовать только в тех функциях, которые опубликованы. Приложение должно определить состояние компонента, вызвав свойство [**феатурестате**](installer-featurestate.md) или [**функции**](installer-features.md) или их эквиваленты API.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсиусефеатурикс**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 





---
description: Метод Инсталлпродукт объекта Installer открывает пакет установщика и инициализирует сеанс установки.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Метод Installer. Инсталлпродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1605fc0f2e955d6f0364159779ae90f8f59e9ace0f3ff14a1106f7623ab7d99d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630396"
---
# <a name="installerinstallproduct-method"></a>Метод Installer. Инсталлпродукт

Метод **инсталлпродукт** объекта [**Installer**](installer-object.md) открывает пакет установщика и инициализирует сеанс установки.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*packagePath* 
</dt> <dd>

Обязательная строка, содержащая путь к установочному пакету.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Необязательная строка, содержащая пары "свойство = значение", разделенные пробелом.

Чтобы выполнить административную установку, включите ACTION = ADMIN в *пропертивалуес*. Дополнительные сведения см. в описании свойства [**Action**](action.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Чтобы полностью удалить продукт, задайте Remove = ALL в *пропертивалуес*. Дополнительные сведения см. в разделе [**Remove**](remove.md) Property.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





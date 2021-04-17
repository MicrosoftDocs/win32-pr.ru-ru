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
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651600"
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

## <a name="remarks"></a>Комментарии

Чтобы полностью удалить продукт, задайте Remove = ALL в *пропертивалуес*. Дополнительные сведения см. в разделе [**Remove**](remove.md) Property.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





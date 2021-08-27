---
description: Метод Опенпродукт объекта Installer открывает пакет установщика для установленного продукта с помощью кода продукта и возвращает объект Session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Метод Installer. Опенпродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129384"
---
# <a name="installeropenproduct-method"></a>Метод Installer. Опенпродукт

Метод **опенпродукт** объекта [**Installer**](installer-object.md) открывает пакет установщика для установленного продукта с помощью кода продукта и возвращает объект [**Session**](session-object.md) .

## <a name="syntax"></a>Синтаксис


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*productCode* 
</dt> <dd>

Обязательная строка, содержащая уникальный код продукта ( [GUID](guid.md)) или дескриптор активации, написанный установщиком.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Обратите внимание, что один процесс может открыть только один объект [**сеанса**](session-object.md) . **Опенпродукт** нельзя использовать в настраиваемом действии, поскольку активная установка является единственным разрешенным сеансом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





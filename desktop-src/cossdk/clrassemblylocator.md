---
description: извлекает сведения о сборке при использовании управляемого кода в платформа .NET Framework среде clr.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Класс Клрассемблилокатор (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: 78f041e8bdc614b1ac6007e21ffbf46ea4afe789a501bb1acefdd21263031859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129276"
---
# <a name="clrassemblylocator-class"></a>Класс Клрассемблилокатор

извлекает сведения о сборке при использовании управляемого кода в платформа .NET Framework среде clr.

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ ассемблилокатор                                 |
| ProgID:     | L "System. EnterpriseServices. internal. Ассемблилокатор" |
| Интерфейсы | [**иассемблилокатор**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Назначение

Используйте этот класс для доступа к методам [**иассемблилокатор**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).

## <a name="remarks"></a>Remarks

Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

чтобы использовать этот класс из Visual Basic майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Клрассемблилокатор можно объявить с помощью "Комсвкслиб. Клрассемблилокатор" в качестве имени класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



 


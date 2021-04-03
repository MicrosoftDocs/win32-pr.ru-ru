---
description: Извлекает сведения о сборке при использовании управляемого кода в платформа .NET Framework среде CLR.
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
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895646"
---
# <a name="clrassemblylocator-class"></a>Класс Клрассемблилокатор

Извлекает сведения о сборке при использовании управляемого кода в платформа .NET Framework среде CLR.

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ ассемблилокатор                                 |
| ProgID:     | L "System. EnterpriseServices. internal. Ассемблилокатор" |
| Интерфейсы | [**иассемблилокатор**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Назначение

Используйте этот класс для доступа к методам [**иассемблилокатор**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).

## <a name="remarks"></a>Комментарии

Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Клрассемблилокатор можно объявить с помощью "Комсвкслиб. Клрассемблилокатор" в качестве имени класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



 


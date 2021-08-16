---
description: Удаляет существующий экземпляр класса из репозитория.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma DeleteInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 29739f1d95cf5c8352c2b7822dbc3da7777f41f69fc5086631e0069c3b832623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316852"
---
# <a name="pragma-deleteinstance"></a>pragma DeleteInstance

Команда **pragma DeleteInstance** удаляет существующий экземпляр класса из репозитория.

Ниже описан синтаксис для этой команды:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* — это уникальный идентификатор экземпляра, который удаляется компилятором MOF из текущего пространства имен.

*\[ Флаг \]* должен быть одним из следующих аргументов.



| Флаг   | Описание                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fail   | Приводит к выходу компилятора MOF с сообщением об ошибке, если класс еще не существует в репозитории. |
| nofail | Приводит к тому, что компилятор MOF продолжит работу, даже если класс еще не существует.                                |



 

## <a name="examples"></a>Примеры

В следующем примере показано, как использовать эту команду.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Команды препроцессора](preprocessor-commands.md)
</dt> </dl>

 

 





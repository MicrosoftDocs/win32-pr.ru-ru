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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080417"
---
# <a name="pragma-deleteinstance"></a>pragma DeleteInstance

Команда **pragma DeleteInstance** удаляет существующий экземпляр класса из репозитория.

Ниже описан синтаксис для этой команды:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* — это уникальный идентификатор экземпляра, который удаляется компилятором MOF из текущего пространства имен.

*\[ Флаг \]* должен быть одним из следующих аргументов.



| Flag   | Описание                                                                                                  |
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

 

 





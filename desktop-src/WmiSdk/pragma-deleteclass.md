---
description: Удаляет существующий класс и его экземпляры из репозитория.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma делетекласс
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913208"
---
# <a name="pragma-deleteclass"></a>pragma делетекласс

Команда препроцессора **pragma делетекласс** удаляет существующий класс и его экземпляры из репозитория.

Ниже описан синтаксис.


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* — имя класса, который компилятор MOF удаляет из текущего пространства имен.

*\[ Флаг \]* должен быть одним из следующих аргументов.



| Flag   | Описание                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fail   | Приводит к выходу компилятора MOF с сообщением об ошибке, если класс еще не существует в репозитории. |
| nofail | Приводит к тому, что компилятор MOF продолжит работу, даже если класс еще не существует.                                |



 

## <a name="examples"></a>Примеры

В следующем примере показано, как использовать эту команду.


```mof
#pragma deleteclass("MyClass1",FAIL)
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

 

 





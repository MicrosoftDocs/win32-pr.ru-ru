---
description: Управляет способом создания или обновления экземпляров в зависимости от указанных флагов.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma инстанцефлагс
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272578"
---
# <a name="pragma-instanceflags"></a>pragma инстанцефлагс

Команда препроцессора **pragma инстанцефлагс** определяет способ создания или обновления экземпляров в зависимости от указанных флагов.

Ниже описан синтаксис.


```mof
#pragma instanceflags ([Flag])
```



*\[ Флаг \]* должен быть одним из следующих аргументов.



| Flag       | Описание                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| креатеонли | Предотвращает изменение компилятором существующих экземпляров в MOF-файле.                                |
| упдатеонли | Запрещает компилятору создавать новые экземпляры, если экземпляр, указанный в MOF-файле, не существует. |



 

## <a name="examples"></a>Примеры

В следующем примере показано, как использовать эту команду.


```mof
#pragma instanceflags("createonly")
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

 

 





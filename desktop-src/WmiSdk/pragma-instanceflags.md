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
ms.openlocfilehash: 107325b329fcc51f474dd3ac9ea3a16e8882ff55114012d87a303ac73647bb37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817990"
---
# <a name="pragma-instanceflags"></a>pragma инстанцефлагс

Команда препроцессора **pragma инстанцефлагс** определяет способ создания или обновления экземпляров в зависимости от указанных флагов.

Ниже описан синтаксис.


```mof
#pragma instanceflags ([Flag])
```



*\[ Флаг \]* должен быть одним из следующих аргументов.



| Флаг       | Описание                                                                                                |
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



## <a name="see-also"></a>См. также

<dl> <dt>

[Команды препроцессора](preprocessor-commands.md)
</dt> </dl>

 

 





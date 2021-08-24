---
title: /Client, параметр
description: Параметр/Client направляет компилятор MIDL для создания исходных файлов C на стороне клиента для интерфейса RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- MIDL/Client Switch
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8361a41aa0e7c87c42eb41508fee0973d6fd4dd821e2008aa2148c8460fc63ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764364"
---
# <a name="client-switch"></a>/Client, параметр

Параметр **/Client** направляет компилятор MIDL для создания исходных файлов C на стороне клиента для интерфейса RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>заглушка * * * *


</dt> <dd>

Создает файлы на стороне клиента.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>нет * * * *


</dt> <dd>

Не создает файлы на стороне клиента.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Если параметр **/Client** не указан, компилятор MIDL создает файл заглушки клиента. Этот параметр не влияет на интерфейсы OLE.

Параметр **/Client** имеет приоритет над параметром [**/cstub**](-cstub.md) .

## <a name="examples"></a>Примеры

**MIDL/Client нет filename. idl**

**MIDL/Client заглушек filename. idl**

## <a name="see-also"></a>См. также

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Server**](-server.md)
</dt> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





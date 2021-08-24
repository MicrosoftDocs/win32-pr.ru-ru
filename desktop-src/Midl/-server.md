---
title: Параметр/Server
description: Параметр/Server направляет компилятор MIDL для создания исходных файлов C на стороне сервера для интерфейса RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- Параметр/Server MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf634e9ce91e937ff1e43b9059d12181dc723695139001ec368109d6fdf4a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067474"
---
# <a name="server-switch"></a>Параметр/Server

Параметр **/Server** направляет компилятор MIDL для создания исходных файлов C на стороне сервера для интерфейса RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>заглушка * * * *


</dt> <dd>

Создает файлы на стороне сервера.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>нет * * * *


</dt> <dd>

Не создает файлы на стороне сервера.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Если параметр **/Server** не указан, компилятор MIDL создает файл заглушки сервера. Этот параметр не влияет на интерфейсы OLE.

Параметр **None** не приводит к созданию файлов.

Параметр **/Server** имеет приоритет над параметром **/sstub** .

## <a name="examples"></a>Примеры

**MIDL/Server нет**

**заглушка с MIDL/Server**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 





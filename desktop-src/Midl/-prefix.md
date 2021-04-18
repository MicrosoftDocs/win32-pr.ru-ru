---
title: /префикс, параметр
description: Параметр/префикс направляет компилятор MIDL к добавлению строк префикса в имена клиента и (или) имени подпрограммы заглушки сервера.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- MIDL/префикс Switch
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532738"
---
# <a name="prefix-switch"></a>/префикс, параметр

Параметр **/префикс** направляет компилятор MIDL к добавлению строк префикса в имена клиента и (или) имени подпрограммы заглушки сервера. Это можно использовать для того, чтобы одна программа была как клиентом, так и сервером того же интерфейса, без возникновения конфликта имен клиентских и серверных подпрограмм.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>Клиент * * * *


</dt> <dd>

Затрагивает только имена подпрограмм клиентской заглушки.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>кстуб * * * *


</dt> <dd>

То же, что и *клиент*. Затрагивает только имена подпрограмм клиентской заглушки.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>сервер * * * *


</dt> <dd>

Затрагивает только имена подпрограмм, вызванных подпрограммой заглушки сервера.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>сстуб * * * *


</dt> <dd>

То же, что и *сервер*. Затрагивает только имена подпрограмм, вызванных подпрограммой заглушки сервера.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>Switch * * * *


</dt> <dd>

Влияет на дополнительный прототип, добавленный в файл заголовка.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>все * * * *


</dt> <dd>

Влияет на имена клиентской и серверной подпрограммы-заглушки.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Если префикс для клиентских подпрограмм отличается от префикса для подпрограмм на стороне сервера, созданный файл заголовка будет содержать как клиентские, так и прототипы подпрограмм на стороне сервера.

Параметр **/префикс** полезен, если один файл заголовка будет использоваться с заглушками из нескольких запусков компилятора MIDL. Это приводит к вызову дополнительных прототипов подпрограмм в файле заголовка.

Во всех случаях префиксы "клиент", "сервер" и "переключить" будут переопределять все.

## <a name="examples"></a>Примеры

**MIDL/префикс клиент "c \_ " сервер "s \_ "**

**MIDL/префикс все «мууу \_ »**

**MIDL/префикс Client "лай \_ "**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





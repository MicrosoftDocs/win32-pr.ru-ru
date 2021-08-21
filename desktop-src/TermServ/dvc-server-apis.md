---
title: API сервера DVC
description: Динамические API сервера виртуальных каналов (DVC) реализуются с помощью сервера подключение к удаленному рабочему столу (RDC) подключения.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f43ab4032e4500732e2f9ee6cfa9a2c17f8b1892e55973ba633758792f00bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353977"
---
# <a name="dvc-server-apis"></a>API сервера DVC

Динамические API сервера виртуальных каналов (DVC) реализуются с помощью сервера подключение к удаленному рабочему столу (RDC) подключения.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**ивтссерверчаннел**](iwtsserverchannel.md)
</dt> <dd>

Этот интерфейс не поддерживается.

</dd> <dt>

[**ивтссерверчаннелманажер**](iwtsserverchannelmanager.md)
</dt> <dd>

Этот интерфейс не поддерживается.

</dd> <dt>

[**тприорити**](tpriority.md)
</dt> <dd>

Это перечисление не используется.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Изменения в поведении для других серверных API

-   API сервера был расширен с помощью дополнительного вызова, который открывает динамический виртуальный канал (DVC). Дополнительный вызов выполняется с помощью функции [**втсвиртуалчаннелопенекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .
-   [**втсвиртуалчаннелреад**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    При использовании этого API с DVC всегда будет находиться в начале данных, считываемых с [**помощью \_ \_ заголовка канала PDU**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header). Это означает, что все считывание должно выполняться по крайней мере в блоке данных **\_ \_ длины канала PDU** , переданном в качестве входного буфера.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Если файловый обработчик для DVC извлекается путем вызова [**втсвиртуалчаннелкуери**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) с параметром *втсвиртуалфилехандле*, будет применяться то же правило. Все операции чтения будут содержать [**\_ \_ заголовок PDU канала**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), а буфер чтения должен быть по крайней мере **размером \_ PDU \_ канала** .

 

 
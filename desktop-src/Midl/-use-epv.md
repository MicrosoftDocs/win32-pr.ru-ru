---
title: use_epv Switch
description: '\_Параметр ЕПВ/TestCleanup используется указывает компилятору MIDL создать код заглушки сервера, вызывающий серверную подпрограмму с помощью вектора точки входа (ЕПВ), а не статического вызова. Использовать этот атрибут не рекомендуется.'
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv параметр MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681605"
---
# <a name="use_epv-switch"></a>/TestCleanup используется \_ ЕПВ Switch

Параметр **\_ ЕПВ/TestCleanup используется** указывает компилятору MIDL создать код заглушки сервера, вызывающий серверную подпрограмму с помощью вектора точки входа (ЕПВ), а не статического вызова. Использовать этот атрибут не рекомендуется.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

Как правило, приложениям требуется статическая связь с серверным приложением. Компилятор MIDL по умолчанию создает такой вызов. Однако если приложению требуется, чтобы серверная заглушка вызывала серверную подпрограмму с помощью ЕПВ, необходимо указать параметр **/TestCleanup используется \_ ЕПВ** . Если указан **параметр \_ ЕПВ/TestCleanup используется** , компилятор MIDL создает значение по умолчанию ЕПВ. Этот ЕПВ по умолчанию используется, если приложение не регистрирует другой ЕПВ через вызов [**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .

## <a name="examples"></a>Примеры

**MIDL/TestCleanup используется \_ ЕПВ** *filename * * *. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/но \_ по умолчанию \_ ЕПВ**](-no-default-epv.md)
</dt> <dt>

[**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 
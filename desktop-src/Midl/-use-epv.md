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
ms.openlocfilehash: 614abaf4c124aa0a6e1ca5f7da347ab4a9a2264e174c91734e6a75b188500a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014062"
---
# <a name="use_epv-switch"></a>/TestCleanup используется \_ ЕПВ Switch

Параметр **\_ ЕПВ/TestCleanup используется** указывает компилятору MIDL создать код заглушки сервера, вызывающий серверную подпрограмму с помощью вектора точки входа (ЕПВ), а не статического вызова. Использовать этот атрибут не рекомендуется.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

Как правило, приложениям требуется статическая связь с серверным приложением. Компилятор MIDL по умолчанию создает такой вызов. Однако если приложению требуется, чтобы серверная заглушка вызывала серверную подпрограмму с помощью ЕПВ, необходимо указать параметр **/TestCleanup используется \_ ЕПВ** . Если указан **параметр \_ ЕПВ/TestCleanup используется** , компилятор MIDL создает значение по умолчанию ЕПВ. Этот ЕПВ по умолчанию используется, если приложение не регистрирует другой ЕПВ через вызов [**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .

## <a name="examples"></a>Примеры

**MIDL/TestCleanup используется \_ ЕПВ** *filename * * *. idl**

## <a name="see-also"></a>См. также

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/но \_ по умолчанию \_ ЕПВ**](-no-default-epv.md)
</dt> <dt>

[**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 
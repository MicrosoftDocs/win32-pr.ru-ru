---
title: no_default_epv Switch
description: Параметр/но \_ по умолчанию \_ ЕПВ указывает компилятору MIDL не создавать вектор точки входа по умолчанию (ЕПВ). Использовать этот атрибут не рекомендуется.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv параметр MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987398"
---
# <a name="no_default_epv-switch"></a>/но \_ параметр ЕПВ по умолчанию \_

Параметр **/но \_ по умолчанию \_ ЕПВ** указывает компилятору MIDL не создавать вектор точки входа по умолчанию (ЕПВ). Использовать этот атрибут не рекомендуется.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Комментарии

В этом случае приложение должно зарегистрировать ЕПВ с помощью вызова [**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) . Сравните этот параметр с параметром [**\_ ЕПВ/TestCleanup используется**](-use-epv.md) .

## <a name="examples"></a>Примеры

**MIDL/но \_ по умолчанию \_ ЕПВ filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/TestCleanup используется \_ ЕПВ**](-use-epv.md)
</dt> <dt>

[**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 
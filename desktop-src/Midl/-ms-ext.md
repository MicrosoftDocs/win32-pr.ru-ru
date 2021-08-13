---
title: ms_ext Switch
description: Начиная с MIDL версии 3,0 функции, включенные с помощью \_ коммутатора MS ext, теперь являются режимом по умолчанию для КОМПИЛЯТОРА MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext параметр MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bee998e96d26c0f5bb2a1e0f28446433681a7175ff181556ad7976c58af356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644563"
---
# <a name="ms_ext-switch"></a>/МС \_ внешний коммутатор

Начиная с MIDL версии 3,0 функции, включенные с помощью коммутатора **MS \_ ext** , теперь являются режимом по умолчанию для компилятора MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

## <a name="remarks"></a>Remarks

Использование параметра не приведет к возникновению ошибки компилятора, поэтому нет необходимости удалять ссылки на **/МС \_ ext** или [**/c \_ ext**](-c-ext.md) из существующего файла makefile.

Следующие расширения Майкрософт для использование DCE теперь доступны по умолчанию:

-   Определения интерфейсов для объектов OLE. Дополнительные сведения о файлах, создаваемых для интерфейсов OLE, см. в разделе [файлы, созданные для COM-интерфейса](files-generated-for-a-com-interface.md) .
-   Атрибут [**\[ обратного вызова \]**](callback.md) , указывающий статическую функцию обратного вызова на клиенте
-   [**\_ цитата cpp**](cpp-quote.md)(*\_ строка в кавычках*) и [**\# pragma MIDL \_ echo**](pragma.md)
-   типы, константы и строки для расширенных символов [**WCHAR \_ t**](wchar-t.md)
-   [**Инициализация перечисления**](enum.md) (разреженные перечислители)
-   Выражения в качестве спецификаторов размера и дискриминатора
-   [Обработка расширений](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Наследование типа атрибута указателя](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Несколько интерфейсов](/windows/desktop/Rpc/registering-interfaces)
-   Определения за пределами блока интерфейса
-   Можно опустить [атрибуты направления](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**в**](in.md), [**out**](out-idl.md)\]

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Наследование типа атрибута указателя](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**\_Конфигурация/АПП**](-app-config.md)
</dt> <dt>

[**/осф**](-osf.md)
</dt> </dl>

 

 
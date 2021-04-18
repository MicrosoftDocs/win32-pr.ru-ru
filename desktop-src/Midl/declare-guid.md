---
title: Ключевое слово declare_guid
description: '\_Ключевое слово Declare GUID предписывает MIDL создавать переменную GUID в создаваемом файле заголовка.'
keywords:
- declare_guid ключевого слова MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105720015"
---
# <a name="declare_guid-keyword"></a>\_ключевое слово Declare GUID

Ключевое слово **Declare \_ GUID** предписывает MIDL создавать переменную GUID в создаваемом файле заголовка.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя переменной* 
</dt> <dd>

Задает имя переменной для идентификатора в создаваемом файле заголовка.

</dd> <dt>

*guid*
</dt> <dd>

Указывает [идентификатор GUID](/windows/win32/api/guiddef/ns-guiddef-guid) , который будет применяться к имени переменной в создаваемом файле заголовка.

</dd> </dl>

## <a name="examples"></a>Примеры

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Комментарии

Использование `declare_guid` эквивалентно использованию `cpp_quote` для создания вызова `EXTERN_GUID` макроса.

Приведенный выше пример приводит к получению следующих выходных данных:

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

`declare_guid`Инструкция предоставляется для удобства. Преимущество этого метода в том, что он использует тот же синтаксис GUID, что и [ `uuid` атрибут](uuid.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**uuid - атрибут**](uuid.md)
</dt> <dt>

[**Структура GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>

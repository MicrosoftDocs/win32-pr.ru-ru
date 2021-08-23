---
description: 'дополнительные сведения: ошибки расширяемых механизмов служба хранилища'
title: ошибки расширенного обработчика служба хранилища
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0c0ee0a4423d5b37913bd7922af07a7b2196a30176b2a1adca37240e03a28594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721464"
---
# <a name="extensible-storage-engine-errors"></a>ошибки расширенного обработчика служба хранилища


_**Применимо к:** Windows | Windows Сервером_

## <a name="extensible-storage-engine-errors"></a>ошибки расширенного обработчика служба хранилища

все возможные ошибки, возвращаемые API-интерфейсом расширяемого служба хранилища Engine (ESE), определяются типом данных [JET_ERR](./jet-err.md) . список флагов ошибок, определенных для этого API, см. в разделе [коды ошибок расширенных служба хранилища Engine](./extensible-storage-engine-error-codes.md).

В документации по API-интерфейсу ESE документированы только наиболее важные ошибки. Эти ошибки обычно представляют ошибки использования API или очень важные условия возникновения ошибок. Имейте в виду, что любой из этих API-интерфейсов ESE также может возвращать другие ошибки, не описанные для каждого API. В таких случаях вызывающий объект должен просто обменять ошибку, как и любые другие ошибки, возвращаемые API. Конкретное значение ошибки может использоваться для диагностики, таких как трассировка.

В общем случае значение, большее нуля, должно интерпретироваться как предупреждение, нулевое значение должно интерпретироваться как успешно, а значение меньше нуля должно интерпретироваться как ошибка. Никакие другие шаблоны в этих значениях (например, диапазоны значений) не должны полагаться на приложения.

Когда ESE обнаруживает некоторые из наиболее серьезных ошибок, она создает запись в журнале событий, содержащую сведения об ошибках. Уровень ведения журнала может управляться [параметрами журнала событий](./event-log-parameters.md).

Некоторым приложениям требуется возможность возвращать [JET_ERR](./jet-err.md)s как HRESULTS. В следующем примере C++ показано, как выполнить это преобразование:

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

Сведения о настройке системных параметров для обработки ошибок см. в разделе [Параметры обработки ошибок](./error-handling-parameters.md).

### <a name="see-also"></a>См. также

[Параметры обработки ошибок](./error-handling-parameters.md)

[коды ошибок расширенного механизма служба хранилища](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)

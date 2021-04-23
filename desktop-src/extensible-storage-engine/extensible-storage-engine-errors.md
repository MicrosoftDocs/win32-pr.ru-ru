---
description: 'Дополнительные сведения: ошибки расширенного подсистемы хранилища'
title: Ошибки расширяемого подсистемы хранилища
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913584"
---
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="426c3-103">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="426c3-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="426c3-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="426c3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="426c3-105">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="426c3-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="426c3-106">Все возможные ошибки, возвращаемые API-интерфейсом модуля расширенного хранилища (ESE), определяются типом данных [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="426c3-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="426c3-107">Список флагов ошибок, определенных для этого API, см. в разделе [расширенные коды ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="426c3-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="426c3-108">В документации по API-интерфейсу ESE документированы только наиболее важные ошибки.</span><span class="sxs-lookup"><span data-stu-id="426c3-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="426c3-109">Эти ошибки обычно представляют ошибки использования API или очень важные условия возникновения ошибок.</span><span class="sxs-lookup"><span data-stu-id="426c3-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="426c3-110">Имейте в виду, что любой из этих API-интерфейсов ESE также может возвращать другие ошибки, не описанные для каждого API.</span><span class="sxs-lookup"><span data-stu-id="426c3-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="426c3-111">В таких случаях вызывающий объект должен просто обменять ошибку, как и любые другие ошибки, возвращаемые API.</span><span class="sxs-lookup"><span data-stu-id="426c3-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="426c3-112">Конкретное значение ошибки может использоваться для диагностики, таких как трассировка.</span><span class="sxs-lookup"><span data-stu-id="426c3-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="426c3-113">В общем случае значение, большее нуля, должно интерпретироваться как предупреждение, нулевое значение должно интерпретироваться как успешно, а значение меньше нуля должно интерпретироваться как ошибка.</span><span class="sxs-lookup"><span data-stu-id="426c3-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="426c3-114">Никакие другие шаблоны в этих значениях (например, диапазоны значений) не должны полагаться на приложения.</span><span class="sxs-lookup"><span data-stu-id="426c3-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="426c3-115">Когда ESE обнаруживает некоторые из наиболее серьезных ошибок, она создает запись в журнале событий, содержащую сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="426c3-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="426c3-116">Уровень ведения журнала может управляться [параметрами журнала событий](./event-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="426c3-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="426c3-117">Некоторым приложениям требуется возможность возвращать [JET_ERR](./jet-err.md)s как HRESULTS.</span><span class="sxs-lookup"><span data-stu-id="426c3-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="426c3-118">В следующем примере C++ показано, как выполнить это преобразование:</span><span class="sxs-lookup"><span data-stu-id="426c3-118">The following C++ example shows how to make that conversion:</span></span>

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

<span data-ttu-id="426c3-119">Сведения о настройке системных параметров для обработки ошибок см. в разделе [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="426c3-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="426c3-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="426c3-120">See Also</span></span>

[<span data-ttu-id="426c3-121">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="426c3-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="426c3-122">Коды ошибок расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="426c3-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="426c3-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="426c3-123">JET_ERR</span></span>](./jet-err.md)

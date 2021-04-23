---
title: Оптимизация атрибута
description: Атрибут \ optimize \ ACF используется для точной настройки уровня градации для маршалирования данных.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- Оптимизация атрибута MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650304"
---
# <a name="optimize-attribute"></a><span data-ttu-id="a22e8-104">Оптимизация атрибута</span><span class="sxs-lookup"><span data-stu-id="a22e8-104">optimize attribute</span></span>

<span data-ttu-id="a22e8-105">Атрибут **\[ optimize \]** ACF используется для точной настройки уровня градации для маршалирования данных.</span><span class="sxs-lookup"><span data-stu-id="a22e8-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="a22e8-106">Это ключевое слово суперцеедед и не должно использоваться.</span><span class="sxs-lookup"><span data-stu-id="a22e8-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="a22e8-107">В текущих компиляциях MIDL вместо этого следует использовать [**/Oicf**](-oi.md)[**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="a22e8-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="a22e8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a22e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22e8-109">*параметры оптимизации*</span><span class="sxs-lookup"><span data-stu-id="a22e8-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="a22e8-110">Указывает метод маршалирования данных.</span><span class="sxs-lookup"><span data-stu-id="a22e8-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="a22e8-111">Используйте "s" для маршалирования в смешанном режиме или "i" для интерпретируемого маршалирования.</span><span class="sxs-lookup"><span data-stu-id="a22e8-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a22e8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a22e8-112">Remarks</span></span>

<span data-ttu-id="a22e8-113">Эта версия RPC предоставляет два метода для маршалирования данных: смешанный режим ("s") и интерпретируемый ("i").</span><span class="sxs-lookup"><span data-stu-id="a22e8-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="a22e8-114">Эти методы соответствуют параметрам командной строки [**/OS**](-os.md) и [**/Oi**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="a22e8-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="a22e8-115">Интерпретируемый метод выполняет передачу данных полностью в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="a22e8-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="a22e8-116">Хотя это может значительно снизить размер заглушки, это может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="a22e8-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="a22e8-117">Если важна производительность, то лучшим подходом может быть метод смешанного режима.</span><span class="sxs-lookup"><span data-stu-id="a22e8-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="a22e8-118">Смешанный режим позволяет компилятору MIDL определить, какие данные будут маршалированы во встроенном виде и что будет маршалирован при вызове в автономную библиотеку динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="a22e8-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="a22e8-119">Если многие процедуры используют одни и те же типы данных, для маршалирования данных можно многократно вызывать одну процедуру.</span><span class="sxs-lookup"><span data-stu-id="a22e8-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="a22e8-120">Таким образом, данные, наиболее подходящие для встроенного маршалирования, обрабатываются в виде встроенных данных, а другие данные могут быть более эффективно упакованы в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="a22e8-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="a22e8-121">Обратите внимание, что атрибут **\[ optimize \]** можно использовать как атрибут интерфейса или как атрибут операции.</span><span class="sxs-lookup"><span data-stu-id="a22e8-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="a22e8-122">Если он используется как атрибут интерфейса, он задает значение по умолчанию для всего интерфейса, переопределяя параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="a22e8-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="a22e8-123">Однако если он используется как атрибут операции, он влияет только на эту операцию, переопределяя параметры командной строки и интерфейс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a22e8-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="a22e8-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="a22e8-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="a22e8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a22e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22e8-126">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="a22e8-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a22e8-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="a22e8-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="a22e8-128">**/OS**</span><span class="sxs-lookup"><span data-stu-id="a22e8-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="a22e8-129">**/robust**</span><span class="sxs-lookup"><span data-stu-id="a22e8-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 





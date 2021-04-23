---
title: Type-Conversion и маршалирование атрибутов ACF
description: Используйте эти атрибуты для управления передачей данных по сети.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF MIDL, атрибуты, преобразование типов и маршалирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986723"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="237b5-104">Type-Conversion и маршалирование атрибутов ACF</span><span class="sxs-lookup"><span data-stu-id="237b5-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="237b5-105">Используйте эти атрибуты для управления передачей данных по сети.</span><span class="sxs-lookup"><span data-stu-id="237b5-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="237b5-106">attribute</span><span class="sxs-lookup"><span data-stu-id="237b5-106">Attribute</span></span>                                        | <span data-ttu-id="237b5-107">Использование</span><span class="sxs-lookup"><span data-stu-id="237b5-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="237b5-108">[**кодировать**](encode.md)[**декодирование**](decode.md)</span><span class="sxs-lookup"><span data-stu-id="237b5-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="237b5-109">Инструктирует MIDL для предоставления подпрограммым типа или сериализации процедур, создаваемых для заглушек.</span><span class="sxs-lookup"><span data-stu-id="237b5-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="237b5-110">Клиентское приложение может вызывать эти подпрограммы для маршалирования данных по значению.</span><span class="sxs-lookup"><span data-stu-id="237b5-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="237b5-111">**представлять \_ как**</span><span class="sxs-lookup"><span data-stu-id="237b5-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="237b5-112">Указывает способ представления типа данных в сети, когда Точная природа типа данных клиента не важна для сервера (поскольку ему требуются только сами данные, а не фактическая структура), или фактический тип клиента неизвестен для MIDL во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="237b5-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="237b5-113">Например, если клиентское приложение использует связанный список чисел с плавающей запятой, можно указать, что в качестве телепередачи этого списка следует использовать массив типа [**float**](float.md).</span><span class="sxs-lookup"><span data-stu-id="237b5-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="237b5-114">**Пользовательская \_ Упаковка**</span><span class="sxs-lookup"><span data-stu-id="237b5-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="237b5-115">Управляет передачей данных по сети путем реализации собственных подпрограмм упаковки.</span><span class="sxs-lookup"><span data-stu-id="237b5-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="237b5-116">Этот атрибут полезен при наличии неизвестного типа данных для MIDL или при передаче информации между платформами с обратным порядком байтов и с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="237b5-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="237b5-117">Атрибуты упаковки DCE [**в \_ строке**](in-line.md) и [**вне \_ \_ строки**](out-of-line.md) не реализуются в Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="237b5-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="237b5-118">Компилятор MIDL автоматически маршалирует сложные типы данных в автономном виде.</span><span class="sxs-lookup"><span data-stu-id="237b5-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 





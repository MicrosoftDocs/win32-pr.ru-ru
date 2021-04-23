---
title: Функция type_UserMarshal
description: Функция Type \_ усермаршал — это вспомогательная функция для атрибутов \ "\ проводное \_ маршалирование \" и \ "пользовательское \_ маршалирование \".
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413656"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="a84e1-104">Тип \_ Усермаршал функция</span><span class="sxs-lookup"><span data-stu-id="a84e1-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="a84e1-105">Функция **<type> \_ усермаршал** является вспомогательной функцией для \[ атрибутов [ \_ маршалирования](/windows/desktop/Midl/wire-marshal) \] и \[ [ \_ маршалирования пользователя](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="a84e1-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="a84e1-106">Заглушки вызывают эту функцию для маршалирования данных на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="a84e1-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="a84e1-107">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a84e1-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="a84e1-108"><type>В имени функции — это усерм-тип, указанный в **\[ \_ \]** определении типа маршалирования или **\[ пользовательской \_ упаковки \]** .</span><span class="sxs-lookup"><span data-stu-id="a84e1-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="a84e1-109">Этот тип может быть непригодным или даже недоступным при использовании с атрибутом **\[ пользовательского \_ маршалирования \]** — типом, неизвестным компилятору MIDL.</span><span class="sxs-lookup"><span data-stu-id="a84e1-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="a84e1-110">Имя типа провода (имя типа трансмиссибле) не используется в прототипе функции.</span><span class="sxs-lookup"><span data-stu-id="a84e1-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="a84e1-111">Однако обратите внимание, что тип провода определяет макет сети для данных, как указано в использование DCE.</span><span class="sxs-lookup"><span data-stu-id="a84e1-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="a84e1-112">Параметр *пфлагс* является указателем на беззнаковое поле с длинным флагом.</span><span class="sxs-lookup"><span data-stu-id="a84e1-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="a84e1-113">Верхнее слово флага содержит флаги представления данных NDR в соответствии с определением использование DCE для чисел с плавающей запятой, порядка байтов и символьных представлений.</span><span class="sxs-lookup"><span data-stu-id="a84e1-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="a84e1-114">В нижнем слове содержится флаг контекста маршалирования, определенный в канале COM.</span><span class="sxs-lookup"><span data-stu-id="a84e1-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="a84e1-115">Точный макет флагов внутри поля описан в [ \_ функции Type усерсизе](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="a84e1-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="a84e1-116">Параметр *pBuffer* является указателем текущего буфера.</span><span class="sxs-lookup"><span data-stu-id="a84e1-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="a84e1-117">Этот указатель может быть или не выдаваться по строке.</span><span class="sxs-lookup"><span data-stu-id="a84e1-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="a84e1-118">Функция **<type> \_ усермаршал** должна правильно выстроить указатель на буфер, маршалировать данные и вернуть новую позиции буфера, которая является адресом первого байта после упакованного объекта.</span><span class="sxs-lookup"><span data-stu-id="a84e1-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="a84e1-119">Помните, что спецификация типа провода определяет фактический макет данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="a84e1-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="a84e1-120">Параметр *пмйобж* является указателем на объект пользовательского типа.</span><span class="sxs-lookup"><span data-stu-id="a84e1-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="a84e1-121">Возвращаемое значение — это новая координата буфера, которая представляет собой адрес первого байта после неупакованного объекта.</span><span class="sxs-lookup"><span data-stu-id="a84e1-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="a84e1-122">Переполнение буфера может произойти при неправильном вычислении размера данных и попытке маршалировать больше данных, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="a84e1-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="a84e1-123">Следует избегать такой ситуации.</span><span class="sxs-lookup"><span data-stu-id="a84e1-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="a84e1-124">Для проверки с помощью указателя, **<type> \_ усермаршал** возвращается.</span><span class="sxs-lookup"><span data-stu-id="a84e1-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="a84e1-125">В противном случае вы рискуете создать исключение переполнения буфера, вызываемое модулем NDR.</span><span class="sxs-lookup"><span data-stu-id="a84e1-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="a84e1-126">Исключения должны быть перехвачены и обработаны локально, исключения не должны быть разрешены для пропигатед стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="a84e1-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a84e1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a84e1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a84e1-128">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="a84e1-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="a84e1-129">проводное \_ маршалирование</span><span class="sxs-lookup"><span data-stu-id="a84e1-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="a84e1-130">Пользовательская \_ Упаковка</span><span class="sxs-lookup"><span data-stu-id="a84e1-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
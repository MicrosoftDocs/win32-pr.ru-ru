---
title: Функция type_UserUnmarshal
description: Функция Type \_ усерунмаршал — это вспомогательная функция для атрибутов \ "\ проводное \_ маршалирование \" и \ "пользовательское \_ маршалирование \".
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070579"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="d98be-104">Тип \_ Усерунмаршал функция</span><span class="sxs-lookup"><span data-stu-id="d98be-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="d98be-105">Функция **<type> \_ усерунмаршал** является вспомогательной функцией для \[ атрибутов [ \_ маршалирования](/windows/desktop/Midl/wire-marshal) \] и \[ [ \_ маршалирования пользователя](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="d98be-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="d98be-106">Заглушки вызывают эту функцию для распаковки данных на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="d98be-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="d98be-107">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d98be-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="d98be-108"><type>В имени функции — это усерм-тип, указанный в **\[ \_ \]** определении типа маршалирования или **\[ пользовательской \_ упаковки \]** .</span><span class="sxs-lookup"><span data-stu-id="d98be-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="d98be-109">Этот тип может быть непригодным или даже при использовании с атрибутом **\[ пользовательской \_ маршалирования \]** , неизвестным компилятору MIDL.</span><span class="sxs-lookup"><span data-stu-id="d98be-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="d98be-110">Имя типа провода (имя типа трансмиссибле) не используется в прототипе функции.</span><span class="sxs-lookup"><span data-stu-id="d98be-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="d98be-111">Однако обратите внимание, что тип провода определяет макет сети для данных, как указано в использование DCE.</span><span class="sxs-lookup"><span data-stu-id="d98be-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="d98be-112">Параметр *пфлагс* является указателем на **беззнаковое поле с длинным** флагом.</span><span class="sxs-lookup"><span data-stu-id="d98be-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="d98be-113">Верхнее слово флага содержит флаги представления данных NDR в соответствии с определением использование DCE для чисел с плавающей запятой, порядка байтов и символьных представлений.</span><span class="sxs-lookup"><span data-stu-id="d98be-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="d98be-114">В нижнем слове содержится флаг контекста маршалирования, определенный в канале COM.</span><span class="sxs-lookup"><span data-stu-id="d98be-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="d98be-115">Точный макет флагов внутри поля описан в [ \_ функции Type усерсизе](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="d98be-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="d98be-116">Параметр *pBuffer* является указателем текущего буфера.</span><span class="sxs-lookup"><span data-stu-id="d98be-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="d98be-117">Этот указатель может быть или не выдаваться по строке.</span><span class="sxs-lookup"><span data-stu-id="d98be-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="d98be-118">Функция **<type> \_ усерунмаршал** должна соответствующим образом согласовать указатель буфера, распаковать данные и вернуть новую позиции буфера, которая является адресом первого байта после неупакованного объекта.</span><span class="sxs-lookup"><span data-stu-id="d98be-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="d98be-119">Параметр *пмйобж* является указателем на объект определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="d98be-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="d98be-120">В разнородной среде модуль NDR выполняет все необходимые преобразования данных перед вызовом функции **<type> \_ усерунмаршал** .</span><span class="sxs-lookup"><span data-stu-id="d98be-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="d98be-121">Обратите внимание, что механизм NDR выполняет преобразование данных в соответствии с определением типа провода, предоставленным для этого типа данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="d98be-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="d98be-122">Флаг указывает представление данных отправителя.</span><span class="sxs-lookup"><span data-stu-id="d98be-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d98be-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d98be-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d98be-124">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="d98be-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="d98be-125">проводное \_ маршалирование</span><span class="sxs-lookup"><span data-stu-id="d98be-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="d98be-126">Пользовательская \_ Упаковка</span><span class="sxs-lookup"><span data-stu-id="d98be-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
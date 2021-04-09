---
title: Функция type_UserFree
description: Функция Type \_ усерфри — это вспомогательная функция для атрибутов \ "\ проводное \_ маршалирование \" и \ "пользовательское \_ маршалирование \".
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791731"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="4510b-104">Тип \_ Усерфри функция</span><span class="sxs-lookup"><span data-stu-id="4510b-104">The type\_UserFree Function</span></span>

<span data-ttu-id="4510b-105">Функция **<type> \_ усерфри** является вспомогательной функцией для \[ атрибутов [ \_ маршалирования](/windows/desktop/Midl/wire-marshal) \] и \[ [ \_ маршалирования пользователя](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="4510b-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="4510b-106">Заглушки вызывают эту функцию для высвобождения данных на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="4510b-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="4510b-107">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4510b-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="4510b-108"><type>В имени функции — это усерм-тип, указанный в **\[ \_ \]** определении типа маршалирования или **\[ пользовательской \_ упаковки \]** .</span><span class="sxs-lookup"><span data-stu-id="4510b-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="4510b-109">Параметр *пфлагс* является указателем на **беззнаковое поле с длинным** флагом.</span><span class="sxs-lookup"><span data-stu-id="4510b-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="4510b-110">Верхнее слово флага содержит флаги представления данных NDR в соответствии с определением использование DCE для чисел с плавающей запятой, порядка байтов и символьных представлений.</span><span class="sxs-lookup"><span data-stu-id="4510b-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="4510b-111">В нижнем слове содержится флаг контекста маршалирования, определенный в канале COM.</span><span class="sxs-lookup"><span data-stu-id="4510b-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="4510b-112">Точный макет флагов внутри поля описан в [ \_ функции Type усерсизе](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="4510b-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="4510b-113">Параметр *пмйобж* является указателем на объект пользовательского типа.</span><span class="sxs-lookup"><span data-stu-id="4510b-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="4510b-114">Модуль NDR освобождает объект верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4510b-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="4510b-115">Вы несете ответственность за освобождение всех объектов, на которые может указывать объект верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4510b-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="4510b-116">Исключения должны быть перехвачены и обработаны локально, исключения не должны быть разрешены для пропигатед стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="4510b-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4510b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4510b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4510b-118">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="4510b-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="4510b-119">проводное \_ маршалирование</span><span class="sxs-lookup"><span data-stu-id="4510b-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="4510b-120">Пользовательская \_ Упаковка</span><span class="sxs-lookup"><span data-stu-id="4510b-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
---
title: c_ext Switch
description: Этот параметр устарел в версии 3,0 компилятора MIDL. Однако использование \_ параметра c ext не приведет к возникновению ошибки компилятора, поэтому нет необходимости удалять ссылки на/МС \_ ext или/c \_ ext из существующего файла makefile.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext параметр MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681560"
---
# <a name="c_ext-switch"></a><span data-ttu-id="1b105-105">/c \_ внешний коммутатор</span><span class="sxs-lookup"><span data-stu-id="1b105-105">/c\_ext switch</span></span>

<span data-ttu-id="1b105-106">Этот параметр устарел в версии 3,0 компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="1b105-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="1b105-107">Однако использование параметра **c \_ ext** не приведет к возникновению ошибки компилятора, поэтому нет необходимости удалять ссылки на [**/МС \_ ext**](-ms-ext.md) или **/c \_ ext** из существующего файла makefile.</span><span class="sxs-lookup"><span data-stu-id="1b105-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="1b105-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="1b105-108">Switch Options</span></span>

<span data-ttu-id="1b105-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1b105-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b105-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b105-110">Remarks</span></span>

<span data-ttu-id="1b105-111">Следующие функции теперь доступны по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="1b105-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="1b105-112">Многие существующие файлы заголовков определяют типы с квалификаторами, например « **FAR** » и « **STDCALL**», которые не входят в устройство DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="1b105-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="1b105-113">Эти компиляторы (и компилятор MIDL в режиме совместимости с DCE) создают ошибки при попытке обработать эти квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="1b105-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="1b105-114">Компилятор MIDL позволяет компилировать IDL-файлы, содержащие эти квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="1b105-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="1b105-115">Квалификаторы типа не влияют на способ передачи данных в сети.</span><span class="sxs-lookup"><span data-stu-id="1b105-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="1b105-116">Можно опустить атрибуты направления, такие как [**\[ in \]**](in.md) или [**\[ out \]**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="1b105-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="1b105-117">В режиме по умолчанию поддерживаются следующие расширения языка C:</span><span class="sxs-lookup"><span data-stu-id="1b105-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="1b105-118">Битовые поля в структурах и объединениях</span><span class="sxs-lookup"><span data-stu-id="1b105-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="1b105-119">Комментарии, начинающиеся с двух символов косой черты (//)</span><span class="sxs-lookup"><span data-stu-id="1b105-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="1b105-120">Внешние объявления</span><span class="sxs-lookup"><span data-stu-id="1b105-120">External declarations</span></span>
-   <span data-ttu-id="1b105-121">Процедуры с многоточием в списке параметров (...)</span><span class="sxs-lookup"><span data-stu-id="1b105-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="1b105-122">На 32-разрядных платформах [**int**](int.md) — это базовый тип с 32-бит. на 16-разрядных платформах тип **int** распознан, но не является типом, поддерживающим удаленное взаимодействие</span><span class="sxs-lookup"><span data-stu-id="1b105-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="1b105-123">Тип [**void \***](void.md) , который не используется в удаленных операциях</span><span class="sxs-lookup"><span data-stu-id="1b105-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="1b105-124">Квалификаторы типа, включая форму с префиксом, сопоставленным с ANSI, содержат два символа подчеркивания: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **дальнее**, **\_ \_ FAR**, **лоаддс**, **\_ \_ лоаддс**, **NEAR**, **\_ \_ NEAR**, **Pascal**, **\_ \_ Pascal**, **STDCALL**, **\_ \_ STDCALL**, **volatile** и **\_ \_ volatile**.</span><span class="sxs-lookup"><span data-stu-id="1b105-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="1b105-125">Дополнительные сведения об квалификаторах объявления см. в документации по Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="1b105-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b105-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b105-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b105-127">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="1b105-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="1b105-128">**/осф**</span><span class="sxs-lookup"><span data-stu-id="1b105-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="1b105-129">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="1b105-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





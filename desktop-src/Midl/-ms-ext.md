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
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069860"
---
# <a name="ms_ext-switch"></a><span data-ttu-id="406ed-104">/МС \_ внешний коммутатор</span><span class="sxs-lookup"><span data-stu-id="406ed-104">/ms\_ext switch</span></span>

<span data-ttu-id="406ed-105">Начиная с MIDL версии 3,0 функции, включенные с помощью коммутатора **MS \_ ext** , теперь являются режимом по умолчанию для компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="406ed-105">Effective with MIDL version 3.0, the features enabled by the **ms\_ext** switch are now the default mode for the MIDL compiler.</span></span>

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a><span data-ttu-id="406ed-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="406ed-106">Switch Options</span></span>

<span data-ttu-id="406ed-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="406ed-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="406ed-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="406ed-108">Remarks</span></span>

<span data-ttu-id="406ed-109">Использование параметра не приведет к возникновению ошибки компилятора, поэтому нет необходимости удалять ссылки на **/МС \_ ext** или [**/c \_ ext**](-c-ext.md) из существующего файла makefile.</span><span class="sxs-lookup"><span data-stu-id="406ed-109">Using the switch will not generate a compiler error, so you do not have to remove references to **/ms\_ext** or [**/c\_ext**](-c-ext.md) from an existing makefile.</span></span>

<span data-ttu-id="406ed-110">Следующие расширения Майкрософт для использование DCE теперь доступны по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="406ed-110">The following Microsoft extensions to OSF DCE are now available by default:</span></span>

-   <span data-ttu-id="406ed-111">Определения интерфейсов для объектов OLE.</span><span class="sxs-lookup"><span data-stu-id="406ed-111">Interface definitions for OLE objects.</span></span> <span data-ttu-id="406ed-112">Дополнительные сведения о файлах, создаваемых для интерфейсов OLE, см. в разделе [файлы, созданные для COM-интерфейса](files-generated-for-a-com-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="406ed-112">For more information on the files generated for OLE interfaces, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md)</span></span>
-   <span data-ttu-id="406ed-113">Атрибут [**\[ обратного вызова \]**](callback.md) , указывающий статическую функцию обратного вызова на клиенте</span><span class="sxs-lookup"><span data-stu-id="406ed-113">A [**\[callback\]**](callback.md) attribute specifying a static callback function on the client</span></span>
-   <span data-ttu-id="406ed-114">[**\_ цитата cpp**](cpp-quote.md)(*\_ строка в кавычках*) и [**\# pragma MIDL \_ echo**](pragma.md)</span><span class="sxs-lookup"><span data-stu-id="406ed-114">[**cpp\_quote**](cpp-quote.md)(*quoted\_string*) and [**\#pragma midl\_echo**](pragma.md)</span></span>
-   <span data-ttu-id="406ed-115">типы, константы и строки для расширенных символов [**WCHAR \_ t**](wchar-t.md)</span><span class="sxs-lookup"><span data-stu-id="406ed-115">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings</span></span>
-   <span data-ttu-id="406ed-116">[**Инициализация перечисления**](enum.md) (разреженные перечислители)</span><span class="sxs-lookup"><span data-stu-id="406ed-116">[**enum initialization**](enum.md) (sparse enumerators)</span></span>
-   <span data-ttu-id="406ed-117">Выражения в качестве спецификаторов размера и дискриминатора</span><span class="sxs-lookup"><span data-stu-id="406ed-117">Expressions as size and discriminator specifiers</span></span>
-   [<span data-ttu-id="406ed-118">Обработка расширений</span><span class="sxs-lookup"><span data-stu-id="406ed-118">Handle extensions</span></span>](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [<span data-ttu-id="406ed-119">Наследование типа атрибута указателя</span><span class="sxs-lookup"><span data-stu-id="406ed-119">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [<span data-ttu-id="406ed-120">Несколько интерфейсов</span><span class="sxs-lookup"><span data-stu-id="406ed-120">Multiple interfaces</span></span>](/windows/desktop/Rpc/registering-interfaces)
-   <span data-ttu-id="406ed-121">Определения за пределами блока интерфейса</span><span class="sxs-lookup"><span data-stu-id="406ed-121">Definitions outside of the interface block</span></span>
-   <span data-ttu-id="406ed-122">Можно опустить [атрибуты направления](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**в**](in.md), [**out**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="406ed-122">You can omit [directional attributes](/windows/desktop/Rpc/directional-parameter-attributes) \[[**in**](in.md), [**out**](out-idl.md)\]</span></span>

## <a name="see-also"></a><span data-ttu-id="406ed-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="406ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="406ed-124">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="406ed-124">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="406ed-125">Наследование типа атрибута указателя</span><span class="sxs-lookup"><span data-stu-id="406ed-125">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[<span data-ttu-id="406ed-126">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="406ed-126">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="406ed-127">**/осф**</span><span class="sxs-lookup"><span data-stu-id="406ed-127">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 
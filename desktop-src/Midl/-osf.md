---
title: /ОСФ, параметр
description: Коммутатор/ОСФ принудительно обеспечивает беспроблемную совместимость с использование DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- MIDL/ОСФ Switch
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069889"
---
# <a name="osf-switch"></a><span data-ttu-id="137f7-104">/ОСФ, параметр</span><span class="sxs-lookup"><span data-stu-id="137f7-104">/osf switch</span></span>

<span data-ttu-id="137f7-105">Коммутатор **/ОСФ** принудительно обеспечивает беспроблемную совместимость с использование DCE.</span><span class="sxs-lookup"><span data-stu-id="137f7-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="137f7-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="137f7-106">Switch Options</span></span>

<span data-ttu-id="137f7-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="137f7-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="137f7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="137f7-108">Remarks</span></span>

<span data-ttu-id="137f7-109">Используйте этот параметр, если приложению требуется обеспечение высокой совместимости с использование DCE для обеспечения переносимости.</span><span class="sxs-lookup"><span data-stu-id="137f7-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="137f7-110">В режиме **/ОСФ** пакет RPCSS автоматически включается при использовании полных указателей, аргументы нуждаются в выделении памяти или при использовании атрибута [**включить \_ выделение**](enable-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="137f7-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="137f7-111">Это означает, что вам не нужно предоставлять пользовательские функции [**пользовательского \_ \_ выделения MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function) и [**MIDL \_ \_**](/windows/desktop/Rpc/the-midl-user-free-function) в клиенте и серверном приложении.</span><span class="sxs-lookup"><span data-stu-id="137f7-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="137f7-112">Следующие расширенные функции Майкрософт недоступны при компиляции с параметром **/ОСФ** :</span><span class="sxs-lookup"><span data-stu-id="137f7-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="137f7-113">Абстрактные деклараторы (безымянные параметры) в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="137f7-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="137f7-114">Определения интерфейса для COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="137f7-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="137f7-115">Имена интерфейсов, длина которых превышает 17 символов.</span><span class="sxs-lookup"><span data-stu-id="137f7-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="137f7-116">Атрибуты только для MIDL, такие как [**\_ маршалирование по сети**](wire-marshal.md), [**\_ маршалирование пользователя**](user-marshal.md)и расширения typelib (ODL).</span><span class="sxs-lookup"><span data-stu-id="137f7-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="137f7-117">Использование ключевых слов ACF в IDL-файле (параметр MIDL **/АПП \_ config** ).</span><span class="sxs-lookup"><span data-stu-id="137f7-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="137f7-118">Статические функции обратного вызова на клиенте.</span><span class="sxs-lookup"><span data-stu-id="137f7-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="137f7-119">Атрибут [**Async**](async.md) .</span><span class="sxs-lookup"><span data-stu-id="137f7-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="137f7-120">[**\_ кавычки cpp**](cpp-quote.md) и **\# pragma MIDL \_ echo**.</span><span class="sxs-lookup"><span data-stu-id="137f7-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="137f7-121">типы, константы и строки для расширенных символов типа [**WCHAR \_ t**](wchar-t.md) .</span><span class="sxs-lookup"><span data-stu-id="137f7-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="137f7-122">инициализация [**перечисления**](enum.md) (разреженные перечислители).</span><span class="sxs-lookup"><span data-stu-id="137f7-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="137f7-123">Спецификация размера только для [**выхода**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="137f7-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="137f7-124">Смешанные указатели размеров и размеры массивов.</span><span class="sxs-lookup"><span data-stu-id="137f7-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="137f7-125">Выражения, используемые для описателей размера и дискриминатора.</span><span class="sxs-lookup"><span data-stu-id="137f7-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="137f7-126">Явные параметры обработки в любой из позиций в списке аргументов.</span><span class="sxs-lookup"><span data-stu-id="137f7-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="137f7-127">В режиме **/ОСФ** компилятор MIDL ищет явный маркер привязки в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="137f7-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="137f7-128">Если первый параметр не является дескриптором привязки и указаны один или несколько дескрипторов контекста, то в качестве дескриптора привязки используется крайний левый дескриптор контекста.</span><span class="sxs-lookup"><span data-stu-id="137f7-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="137f7-129">Если первый параметр не является дескриптором и дескрипторы контекста отсутствуют, процедура использует неявную привязку с помощью [**неявного \_ дескриптора**](implicit-handle.md) или [**автоматической \_ обработки**](auto-handle.md)атрибута ACF.</span><span class="sxs-lookup"><span data-stu-id="137f7-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="137f7-130">Наследование типа атрибута Pointer.</span><span class="sxs-lookup"><span data-stu-id="137f7-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="137f7-131">Использование DCE не допускает указателей без атрибутов.</span><span class="sxs-lookup"><span data-stu-id="137f7-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="137f7-132">Поэтому в режиме **/ОСФ** каждый IDL-файл должен определять атрибуты для своих указателей.</span><span class="sxs-lookup"><span data-stu-id="137f7-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="137f7-133">Если какой-либо указатель не имеет явного атрибута, IDL-файл должен иметь спецификацию [**указателя \_ по умолчанию**](pointer-default.md) , чтобы установить тип указателя.</span><span class="sxs-lookup"><span data-stu-id="137f7-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="137f7-134">Несколько интерфейсов в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="137f7-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="137f7-135">Определения за пределами блока Interface.</span><span class="sxs-lookup"><span data-stu-id="137f7-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="137f7-136">Введите квалификаторы, такие как **FAR** и **STDCALL**.</span><span class="sxs-lookup"><span data-stu-id="137f7-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="137f7-137">Пропуск атрибутов направления.</span><span class="sxs-lookup"><span data-stu-id="137f7-137">Omitting directional attributes.</span></span>

<span data-ttu-id="137f7-138">Следующие расширения языка C/C++ недоступны при компиляции с параметром **/ОСФ** :</span><span class="sxs-lookup"><span data-stu-id="137f7-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="137f7-139">Битовые поля в структурах и объединениях.</span><span class="sxs-lookup"><span data-stu-id="137f7-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="137f7-140">Однострочные комментарии разделяются двумя символами косой черты (//).</span><span class="sxs-lookup"><span data-stu-id="137f7-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="137f7-141">Внешние объявления.</span><span class="sxs-lookup"><span data-stu-id="137f7-141">External declarations.</span></span>
-   <span data-ttu-id="137f7-142">Процедуры с многоточием в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="137f7-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="137f7-143">Тип [**int**](int.md).</span><span class="sxs-lookup"><span data-stu-id="137f7-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="137f7-144">Тип **void \*** (за исключением [**атрибута \_ Handle контекста**](context-handle.md) ).</span><span class="sxs-lookup"><span data-stu-id="137f7-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="137f7-145">Квалификаторы типов, включая форму с префиксом, совместимым с ANSI, содержат два символа подчеркивания: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Export** **, Export,** **\_ \_ дальнее**, **далеко**, **\_ \_ лоаддс**, **лоаддс**, **\_ \_ NEAR**, **NEAR**, **\_ \_ Pascal**, **Pascal**, **\_ \_ STDCALL**, **STDCALL**, **\_ \_ volatile** и **volatile**.</span><span class="sxs-lookup"><span data-stu-id="137f7-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="137f7-146">Любая \# [**директива pragma**](pragma.md) warning или **\# pragma** Comment.</span><span class="sxs-lookup"><span data-stu-id="137f7-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="137f7-147">Сериализация типов.</span><span class="sxs-lookup"><span data-stu-id="137f7-147">Type serialization.</span></span>
-   <span data-ttu-id="137f7-148">Тип данных [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="137f7-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="137f7-149">Параметр [**/протокол**](-protocol.md) и синтаксис инструкции ndr64.</span><span class="sxs-lookup"><span data-stu-id="137f7-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="137f7-150">Примеры</span><span class="sxs-lookup"><span data-stu-id="137f7-150">Examples</span></span>

<span data-ttu-id="137f7-151">**MIDL/ОСФ filename. idl**</span><span class="sxs-lookup"><span data-stu-id="137f7-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="137f7-152">**MIDL/ОСФ/АПП \_ config имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="137f7-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="137f7-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="137f7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137f7-154">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="137f7-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="137f7-155">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="137f7-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="137f7-156">**/МС \_ ext**</span><span class="sxs-lookup"><span data-stu-id="137f7-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="137f7-157">Пакет управления памятью RPCSS</span><span class="sxs-lookup"><span data-stu-id="137f7-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 
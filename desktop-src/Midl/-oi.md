---
title: /Oi, параметр
description: /Oi и/ОИК переключает компилятор MIDL на использование полностью интерпретируемого метода маршалирования. Параметр/Oicf обеспечивает дополнительные улучшения производительности.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- MIDL/Oi Switch
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260524"
---
# <a name="oi-switch"></a><span data-ttu-id="0b3ad-105">/Oi, параметр</span><span class="sxs-lookup"><span data-stu-id="0b3ad-105">/Oi switch</span></span>

<span data-ttu-id="0b3ad-106">**/Oi** и **/ОИК** переключает компилятор MIDL на использование полностью интерпретируемого метода маршалирования.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="0b3ad-107">Параметр **/Oicf** обеспечивает дополнительные улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="0b3ad-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="0b3ad-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0b3ad-109">*Oi*</span><span class="sxs-lookup"><span data-stu-id="0b3ad-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3ad-110">Указывает полностью интерпретируемый метод для упаковки кода заглушки, передаваемого между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="0b3ad-111">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-111">This switch is obsolete.</span></span> <span data-ttu-id="0b3ad-112">Рекомендуется использовать вместо него параметр **/Oicf** .</span><span class="sxs-lookup"><span data-stu-id="0b3ad-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="0b3ad-113">*оик*</span><span class="sxs-lookup"><span data-stu-id="0b3ad-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3ad-114">Указывает прокси-метод без кода для маршалирования, который предоставляет все функции **/Oi** , а также еще больше сокращает размер кода заглушки клиента для интерфейсов объектов.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="0b3ad-115">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-115">This switch is obsolete.</span></span> <span data-ttu-id="0b3ad-116">Рекомендуется использовать вместо него параметр **/Oicf** .</span><span class="sxs-lookup"><span data-stu-id="0b3ad-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="0b3ad-117">*ОИФ или Оикф*</span><span class="sxs-lookup"><span data-stu-id="0b3ad-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3ad-118">Указывает прокси-метод для упаковки без кода, который включает все функции, предоставляемые **/Oi** и **/ОИК** , но использует новый интерпретатор (строки быстрого формата), обеспечивающий лучшую производительность, чем **/Oi** или **/ОИК**.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="0b3ad-119">Этот параметр включает последние усовершенствования RPC и рекомендуется для современных сценариев RPC.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b3ad-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b3ad-120">Remarks</span></span>

<span data-ttu-id="0b3ad-121">Обратите внимание на ограничения, связанные с поддерживающими платформами.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="0b3ad-122">Компилятор MIDL 3,0 предоставляет два метода для маршалирования кода: полностью интерпретируемые ( **/Oi**, **/ОИК** и **/Oicf**) и смешанный режим ( [**/OS**](-os.md)).</span><span class="sxs-lookup"><span data-stu-id="0b3ad-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="0b3ad-123">Начиная с MIDL версии 6.0.359, компилятор MIDL по умолчанию создает заглушки **/Oicf** в  [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="0b3ad-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="0b3ad-124">Некоторые функции языка не поддерживаются в некоторых режимах.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="0b3ad-125">В этом случае компилятор автоматически переключается в соответствующий режим и выдает предупреждение.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="0b3ad-126">Если важна производительность, лучшим подходом может быть метод со смешанным режимом ( [**/OS**](-os.md)).</span><span class="sxs-lookup"><span data-stu-id="0b3ad-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="0b3ad-127">В этом режиме компилятор выбирает упаковку некоторых параметров, встроенных в созданные заглушки.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="0b3ad-128">Хотя это приводит к увеличению размера заглушки, оно обеспечивает повышенную производительность.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="0b3ad-129">Полностью интерпретируемый метод маршалирует данные полностью в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="0b3ad-130">Это значительно сокращает размер кода заглушки, но приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="0b3ad-131">Кроме того, при использовании полностью интерпретируемого метода для каждой процедуры существует ограничение в 16 параметров.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="0b3ad-132">Любая процедура, содержащая более 16 параметров, будет автоматически обработана в режиме [**/OS**](-os.md) .</span><span class="sxs-lookup"><span data-stu-id="0b3ad-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="0b3ad-133">В интерпретированных режимах **/Oicf** обеспечивает наилучшую производительность и **/Oi** обеспечивает лучшую обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="0b3ad-134">Вы можете использовать параметр **/OIF** , если приложение использует функции MIDL, появившиеся в MIDL 3,0, например \[ [**\_**](wire-marshal.md) \] атрибуты передачи и \[ [**\_ маршалирования пользователя**](user-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="0b3ad-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="0b3ad-135">Если приложение использует [каналы](/windows/desktop/Rpc/pipes) , необходимо использовать параметр **/OIF** . Если указан другой режим, компилятор MIDL переключается на **/OIF**.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="0b3ad-136">Для точной настройки способа маршалирования кода заглушки Microsoft RPC предоставляет \[ атрибут [**оптимизации**](optimize.md) ACF \] .</span><span class="sxs-lookup"><span data-stu-id="0b3ad-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="0b3ad-137">Этот атрибут используется в качестве атрибута интерфейса или атрибута операции для выбора режима маршалирования для отдельных интерфейсов или для отдельных операций.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="0b3ad-138">Соглашения о вызовах</span><span class="sxs-lookup"><span data-stu-id="0b3ad-138">Calling Conventions</span></span>

<span data-ttu-id="0b3ad-139">Суррогаты, созданные компилятором MIDL в интерпретированном методе с использованием ключей **/Oi**, **/ОИК** или **/OIF** , должны быть скомпилированы в виде процедуры stdcall или cdecl во время компиляции C.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="0b3ad-140">Соглашение о вызовах PASCAL или fastcall не будет работать.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="0b3ad-141">Кроме того, заглушку сервера необходимо скомпилировать как STDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b3ad-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="0b3ad-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="0b3ad-142">Examples</span></span>

<span data-ttu-id="0b3ad-143">**MIDL/Oi filename. idl**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="0b3ad-144">**MIDL/ОИК filename. idl**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="0b3ad-145">**MIDL/OIF filename. idl**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0b3ad-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b3ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3ad-147">**/robust**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="0b3ad-148">**/но \_ надежность**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="0b3ad-149">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="0b3ad-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0b3ad-150">**/OS**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="0b3ad-151">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="0b3ad-152">**/но в \_ формате \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="0b3ad-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 
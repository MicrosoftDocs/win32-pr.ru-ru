---
title: Параметр/OS
description: Параметр/OS указывает смешанный метод для маршалирования кода заглушки, передаваемого между клиентом и сервером.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- Параметр/OS MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672195"
---
# <a name="os-switch"></a><span data-ttu-id="939d1-104">Параметр/OS</span><span class="sxs-lookup"><span data-stu-id="939d1-104">/Os switch</span></span>

<span data-ttu-id="939d1-105">Параметр **/OS** указывает смешанный метод для маршалирования кода заглушки, передаваемого между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="939d1-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="939d1-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="939d1-106">Switch Options</span></span>

<span data-ttu-id="939d1-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="939d1-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="939d1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="939d1-108">Remarks</span></span>

<span data-ttu-id="939d1-109">Перед выбором метода для маршалирования кода необходимо учитывать важные моменты.</span><span class="sxs-lookup"><span data-stu-id="939d1-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="939d1-110">Эти проблемы связаны с размером и производительностью.</span><span class="sxs-lookup"><span data-stu-id="939d1-110">These issues concern size and performance.</span></span> <span data-ttu-id="939d1-111">Компилятор MIDL предоставляет два метода для маршалирования кода: смешанный режим (**/OS**) и полную интерпретацию ([**/Oi**](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="939d1-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="939d1-112">Полностью интерпретируемый метод маршалирует данные полностью в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="939d1-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="939d1-113">Это значительно сокращает размер кода заглушки, но также приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="939d1-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="939d1-114">Используйте MIDL режима по умолчанию **/Oicf** /robust для всех целей, кроме обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="939d1-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="939d1-115">Этот режим является безопасным стандартным режимом компилятора MIDL; любой другой режим следует использовать только после тщательного рассмотрения в отношении безопасности, учитывая, что будущие расширения будут реализованы только в режиме по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="939d1-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="939d1-116">В смешанном режиме компилятор маршалирует некоторые параметры встроенными в созданные заглушки.</span><span class="sxs-lookup"><span data-stu-id="939d1-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="939d1-117">Хотя это приводит к увеличению размера заглушки, это также может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="939d1-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="939d1-118">MIDL обеспечивает полную поддержку многомерных массивов и многомерных указателей только в режиме [**/Oicf**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="939d1-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="939d1-119">В режимах **/OS** и **/Oi** компилятор поддерживает простые варианты, такие как массивы фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="939d1-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="939d1-120">Использование многомерных массивов в режимах **/OS** и **/Oi** может привести к неправильному маршалировании параметров.</span><span class="sxs-lookup"><span data-stu-id="939d1-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="939d1-121">Корпорация Майкрософт рекомендует использовать параметр командной строки **/Oicf** , если интерфейс определяет параметры многомерных массивов или многомерных указателей.</span><span class="sxs-lookup"><span data-stu-id="939d1-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="939d1-122">Чтобы дополнительно определить уровень градации при маршалировании данных, эта версия RPC предоставляет \[ [](optimize.md) \] атрибут optimize.</span><span class="sxs-lookup"><span data-stu-id="939d1-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="939d1-123">Этот атрибут используется в качестве атрибута интерфейса ACF или атрибута операции для выбора режима маршалирования.</span><span class="sxs-lookup"><span data-stu-id="939d1-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="939d1-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="939d1-124">Examples</span></span>

<span data-ttu-id="939d1-125">**MIDL/OS filename. idl**</span><span class="sxs-lookup"><span data-stu-id="939d1-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="939d1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="939d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939d1-127">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="939d1-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="939d1-128">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="939d1-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="939d1-129">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="939d1-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="939d1-130">**/но в \_ формате \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="939d1-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 





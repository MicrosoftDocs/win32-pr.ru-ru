---
title: атрибут enable_allocate
description: Атрибут \ Enable \_ allocate \ ACF указывает, что код заглушки сервера должен включать среду управления памятью заглушки.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate атрибута MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133739"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="a582b-104">включить \_ атрибут выделения</span><span class="sxs-lookup"><span data-stu-id="a582b-104">enable\_allocate attribute</span></span>

<span data-ttu-id="a582b-105">Атрибут **\[ включить \_ выделение \]** ACF указывает, что код заглушки сервера должен включать среду управления памятью заглушки.</span><span class="sxs-lookup"><span data-stu-id="a582b-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="a582b-106">Атрибут **\[ включения \_ выделения \]** устарел и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a582b-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="a582b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a582b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a582b-108">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="a582b-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a582b-109">Задает список из нуля или нескольких дополнительных атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="a582b-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a582b-110">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="a582b-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a582b-111">Имя интерфейса, к которому будет применен атрибут **\[ Enable \_ аллкоате \]** .</span><span class="sxs-lookup"><span data-stu-id="a582b-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a582b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a582b-112">Remarks</span></span>

<span data-ttu-id="a582b-113">В режиме по умолчанию заглушка сервера включает среду памяти, только если используется атрибут **\[ включения \_ выделения \]** .</span><span class="sxs-lookup"><span data-stu-id="a582b-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="a582b-114">Для выделения памяти с помощью [**рпксмаллокате**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate)необходимо включить среду управления памятью.</span><span class="sxs-lookup"><span data-stu-id="a582b-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="a582b-115">В режиме **Использование** (при компиляции с использованием параметра [**/ОСФ**](-osf.md) ) заглушка включает эту среду автоматически или по запросу, когда используется атрибут **\[ включения \_ выделения \]** .</span><span class="sxs-lookup"><span data-stu-id="a582b-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="a582b-116">Заглушка на стороне клиента может быть чувствительна к среде управления памятью **RPCSS** .</span><span class="sxs-lookup"><span data-stu-id="a582b-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="a582b-117">Если конфиденциальная клиентская заглушка выполняется при отключенном пакете **RPCSS** , вызывается распределитель и освобождение пользователей по умолчанию (например, [MIDL, \_ \_ выделяющий](/windows/desktop/Rpc/the-midl-user-allocate-function)пользователя /  [MIDL, \_ \_ свободно](/windows/desktop/Rpc/the-midl-user-free-function)).</span><span class="sxs-lookup"><span data-stu-id="a582b-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="a582b-118">Если этот параметр включен, пакет **RPCSS** использует пару распределителя и дераспределения из пакета.</span><span class="sxs-lookup"><span data-stu-id="a582b-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="a582b-119">В режиме по умолчанию клиент учитывается только в том случае, если используется атрибут **\[ включения \_ выделения \]** .</span><span class="sxs-lookup"><span data-stu-id="a582b-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="a582b-120">Как правило, заглушка на стороне клиента работает в отключенной среде.</span><span class="sxs-lookup"><span data-stu-id="a582b-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="a582b-121">В режиме **Использование** (при компиляции с использованием параметра [**/ОСФ**](-osf.md) ) клиент всегда чувствителен к среде управления памятью **RPCSS** и, следовательно, атрибут **\[ включения \_ выделения \]** не влияет на заглушки клиента.</span><span class="sxs-lookup"><span data-stu-id="a582b-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="a582b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a582b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a582b-123">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="a582b-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a582b-124">\_пользовательское \_ выделение MIDL</span><span class="sxs-lookup"><span data-stu-id="a582b-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="a582b-125">\_бесплатный пользователь \_ MIDL</span><span class="sxs-lookup"><span data-stu-id="a582b-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="a582b-126">**/осф**</span><span class="sxs-lookup"><span data-stu-id="a582b-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="a582b-127">рпксмдисаблеаллокате</span><span class="sxs-lookup"><span data-stu-id="a582b-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="a582b-128">рпксменаблеаллокате</span><span class="sxs-lookup"><span data-stu-id="a582b-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="a582b-129">рпксмфри</span><span class="sxs-lookup"><span data-stu-id="a582b-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 
---
title: Атрибуты заголовка интерфейса
description: Включите эти атрибуты в заголовок интерфейса, чтобы передать сведения обо всем интерфейсе.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL, атрибуты, заголовок интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067780"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="f8ff4-104">Атрибуты заголовка интерфейса</span><span class="sxs-lookup"><span data-stu-id="f8ff4-104">Interface Header Attributes</span></span>

<span data-ttu-id="f8ff4-105">Включите эти атрибуты в заголовок интерфейса, чтобы передать сведения обо всем интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="f8ff4-106">attribute</span><span class="sxs-lookup"><span data-stu-id="f8ff4-106">Attribute</span></span>                                   | <span data-ttu-id="f8ff4-107">Использование</span><span class="sxs-lookup"><span data-stu-id="f8ff4-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8ff4-108">**асинхронный \_ UUID**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="f8ff4-109">Направляет компилятор MIDL для определения синхронных и асинхронных версий COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="f8ff4-110">**UUID**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="f8ff4-111">Обозначает 128-разрядное значение, которое отличает определенный интерфейс от других.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="f8ff4-112">Фактическое значение может представлять GUID, CLSID или IID.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="f8ff4-113">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-113">**local**</span></span>](local.md)                      | <span data-ttu-id="f8ff4-114">Указывает компилятору MIDL создавать только файлы заголовков.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="f8ff4-115">Интерфейс должен иметь либо [**UUID**](uuid.md) , либо [**локальный**](local.md) атрибут.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="f8ff4-116">**MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="f8ff4-117">Управляет выравниванием ОНД неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="f8ff4-118">Используется для обратной совместимости с интерфейсами, созданными на основе MIDL 1,0 или 2,0.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="f8ff4-119">**объектами**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-119">**object**</span></span>](object.md)                    | <span data-ttu-id="f8ff4-120">Определяет интерфейс как COM-интерфейс и направляет компилятору MIDL запрос на создание кода прокси или заглушки вместо заглушек клиента и сервера RPC.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="f8ff4-121">**Версия**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-121">**version**</span></span>](version.md)                  | <span data-ttu-id="f8ff4-122">Определяет конкретную версию интерфейса в случаях, когда существует несколько версий интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="f8ff4-123">Поскольку COM-интерфейсы являются неизменяемыми, нельзя использовать атрибут [**Version**](version.md) в интерфейсе [**объектов**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ff4-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="f8ff4-124">**Указатель \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="f8ff4-125">Указывает тип указателя по умолчанию для всех указателей, кроме тех, которые входят в списки параметров.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="f8ff4-126">Тип по умолчанию может быть [**уникальным**](unique.md), [**ref**](ref.md)или [**ptr**](ptr.md).</span><span class="sxs-lookup"><span data-stu-id="f8ff4-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="f8ff4-127">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="f8ff4-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="f8ff4-128">Задает статическую (хорошо известную) конечную точку, на которой серверное приложение будет прослушивать удаленные вызовы процедур.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="f8ff4-129">См. раздел [атрибуты библиотеки типов](type-library-attributes.md) для атрибутов интерфейса, таких как [**Dual**](dual.md) и [**oleautomation**](oleautomation.md), которые относятся к интерфейсам, определенным или упоминаемым в операторе Library.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 





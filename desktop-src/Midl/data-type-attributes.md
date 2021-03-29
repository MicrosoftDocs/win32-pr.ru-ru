---
title: Атрибуты типа данных
description: Эти атрибуты можно применить к типам данных в операторе typedef, чтобы дополнительно определить использование или воздействие типа данных.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL, атрибуты, тип данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779904"
---
# <a name="data-type-attributes"></a><span data-ttu-id="4896c-104">Атрибуты типа данных</span><span class="sxs-lookup"><span data-stu-id="4896c-104">Data Type Attributes</span></span>

<span data-ttu-id="4896c-105">Эти атрибуты можно применить к типам данных в операторе [**typedef**](typedef.md) , чтобы дополнительно определить использование или воздействие типа данных.</span><span class="sxs-lookup"><span data-stu-id="4896c-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="4896c-106">attribute</span><span class="sxs-lookup"><span data-stu-id="4896c-106">Attribute</span></span>                                 | <span data-ttu-id="4896c-107">Использование</span><span class="sxs-lookup"><span data-stu-id="4896c-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4896c-108">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="4896c-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="4896c-109">Определяет маркер привязки, который хранит сведения о состоянии (контекста) на определенном сервере между вызовами удаленных процедур из определенного клиента.</span><span class="sxs-lookup"><span data-stu-id="4896c-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="4896c-110">Недопустимый для функций [**объектного**](object.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4896c-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="4896c-111">**справиться**</span><span class="sxs-lookup"><span data-stu-id="4896c-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="4896c-112">Указывает настраиваемый тип обработчика, относящийся к приложению.</span><span class="sxs-lookup"><span data-stu-id="4896c-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4896c-113">**MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="4896c-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="4896c-114">Управляет выравниванием ОНД неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="4896c-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="4896c-115">Используйте в [**typedef**](typedef.md)для обеспечения обратной совместимости с интерфейсами, созданными с помощью MIDL 1,0 или 2,0.</span><span class="sxs-lookup"><span data-stu-id="4896c-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="4896c-116">**дать**</span><span class="sxs-lookup"><span data-stu-id="4896c-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="4896c-117">Разрешает передачу открытого потока типизированных данных по удаленному вызову процедуры.</span><span class="sxs-lookup"><span data-stu-id="4896c-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="4896c-118">Параметр [**in**](in.md) pipe позволяет серверу получать поток данных от клиента во время удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="4896c-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="4896c-119">Параметр [**out**](-out.md) pipe позволяет серверу передать поток данных обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="4896c-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="4896c-120">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="4896c-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="4896c-121">Указывает, как тип данных будет передаваться по сети, используемый для настраиваемого маршалирования.</span><span class="sxs-lookup"><span data-stu-id="4896c-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="4896c-122">**\_перечисление v1**</span><span class="sxs-lookup"><span data-stu-id="4896c-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="4896c-123">Указывает, что указанный перечисляемый тип передается как 32-разрядная сущность, а не как 16-разрядное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4896c-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="4896c-124">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="4896c-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="4896c-125">Аналогично [**передаче \_**](transmit-as.md) , но вы реализуете подпрограммы для изменения размера, маршалирования, распаковки и освобождения данных.</span><span class="sxs-lookup"><span data-stu-id="4896c-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 





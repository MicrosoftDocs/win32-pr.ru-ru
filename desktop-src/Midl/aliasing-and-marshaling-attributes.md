---
title: Атрибуты присвоения псевдонимов и маршалирования
description: Распределенные приложения практически всегда передают данные между клиентскими и серверными программами при вызове процедур интерфейса.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL, атрибуты MIDL, присвоение псевдонимов и маршалирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068555"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="47c37-104">Атрибуты присвоения псевдонимов и маршалирования</span><span class="sxs-lookup"><span data-stu-id="47c37-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="47c37-105">Распределенные приложения практически всегда передают данные между клиентскими и серверными программами при вызове процедур интерфейса.</span><span class="sxs-lookup"><span data-stu-id="47c37-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="47c37-106">Разработчики используют MIDL для описания данных, которые клиентские и серверные программы проходят стандартным образом.</span><span class="sxs-lookup"><span data-stu-id="47c37-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="47c37-107">Компилятор MIDL создает заглушку приложения или прокси-сервер, программы для клиента и сервера, которые преобразуют данные в стандартизованную форму, которую можно отправить по сети.</span><span class="sxs-lookup"><span data-stu-id="47c37-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="47c37-108">Формат представления данных в сети (NDR) часто называется форматом подключения данных.</span><span class="sxs-lookup"><span data-stu-id="47c37-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="47c37-109">Заглушки должны преобразовывать данные из собственного формата в памяти программы в NDR.</span><span class="sxs-lookup"><span data-stu-id="47c37-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="47c37-110">Это преобразование называется упаковкой данных.</span><span class="sxs-lookup"><span data-stu-id="47c37-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="47c37-111">Когда клиентская или серверная программа получает данные, она должна преобразовать данные из ОНД в собственный формат для этой программы.</span><span class="sxs-lookup"><span data-stu-id="47c37-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="47c37-112">Это называется распаковкой данных.</span><span class="sxs-lookup"><span data-stu-id="47c37-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="47c37-113">Используйте атрибуты присвоения псевдонимов и маршалирования для управления тем, как данные упаковываются в формат NDR и передаются по сети.</span><span class="sxs-lookup"><span data-stu-id="47c37-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="47c37-114">attribute</span><span class="sxs-lookup"><span data-stu-id="47c37-114">Attribute</span></span>                             | <span data-ttu-id="47c37-115">Использование</span><span class="sxs-lookup"><span data-stu-id="47c37-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47c37-116">**вызвать \_ как**</span><span class="sxs-lookup"><span data-stu-id="47c37-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="47c37-117">Сопоставляет неудаленную функцию с удаленным вызовом процедуры.</span><span class="sxs-lookup"><span data-stu-id="47c37-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="47c37-118">**IID \_ —**</span><span class="sxs-lookup"><span data-stu-id="47c37-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="47c37-119">Предоставляет идентификатор интерфейса COM, который является объектом указателя.</span><span class="sxs-lookup"><span data-stu-id="47c37-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="47c37-120">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="47c37-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="47c37-121">Преобразует тип данных в более простой тип для передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="47c37-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="47c37-122">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="47c37-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="47c37-123">Аналогично [**передаче \_**](transmit-as.md) , но вы реализуете подпрограммы для изменения размера, маршалирования, распаковки и освобождения данных.</span><span class="sxs-lookup"><span data-stu-id="47c37-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="47c37-124">См. также</span><span class="sxs-lookup"><span data-stu-id="47c37-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47c37-125">Преобразование типов и маршалирование атрибутов ACF</span><span class="sxs-lookup"><span data-stu-id="47c37-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 





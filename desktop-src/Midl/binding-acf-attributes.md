---
title: Привязка атрибутов ACF
description: Укажите способ подключения клиента к серверу для удаленных вызовов процедур с атрибутами, перечисленными в следующей таблице.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL, атрибуты, привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068372"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="526c5-104">Привязка атрибутов ACF</span><span class="sxs-lookup"><span data-stu-id="526c5-104">Binding ACF Attributes</span></span>

<span data-ttu-id="526c5-105">Укажите способ подключения клиента к серверу для удаленных вызовов процедур с атрибутами, перечисленными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="526c5-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="526c5-106">attribute</span><span class="sxs-lookup"><span data-stu-id="526c5-106">Attribute</span></span>                                                          | <span data-ttu-id="526c5-107">Использование</span><span class="sxs-lookup"><span data-stu-id="526c5-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="526c5-108">**async**</span><span class="sxs-lookup"><span data-stu-id="526c5-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="526c5-109">Определяет маркер, позволяющий вызывающему объекту выполнить асинхронный вызов и вернуть его немедленно без ожидания результатов, а затем повторно выполнить синхронизацию с вызываемой функцией для получения данных после завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="526c5-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="526c5-110">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="526c5-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="526c5-111">Указывает, что MIDL позволяет коду заглушки автоматически управлять привязкой.</span><span class="sxs-lookup"><span data-stu-id="526c5-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="526c5-112">Это значение по умолчанию, если не указан какой-либо маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="526c5-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="526c5-113">**несериализуемый контекстный \_ обработчик \_**</span><span class="sxs-lookup"><span data-stu-id="526c5-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="526c5-114">Гарантирует, что дескриптор контекста не будет сериализован, независимо от поведения приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="526c5-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="526c5-115">**\_сериализация обработчика контекста \_**</span><span class="sxs-lookup"><span data-stu-id="526c5-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="526c5-116">Гарантирует, что дескриптор контекста будет всегда сериализован независимо от поведения приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="526c5-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="526c5-117">**явный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="526c5-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="526c5-118">Позволяет клиентскому приложению управлять привязкой с помощью явного параметра в каждой процедуре.</span><span class="sxs-lookup"><span data-stu-id="526c5-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="526c5-119">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="526c5-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="526c5-120">Задает маркер для процедур, не имеющих явных параметров Handle.</span><span class="sxs-lookup"><span data-stu-id="526c5-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="526c5-121">Клиентское приложение по-прежнему управляет привязкой.</span><span class="sxs-lookup"><span data-stu-id="526c5-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="526c5-122">**Нечеткий \_ Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="526c5-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="526c5-123">Гарантирует, что методы в интерфейсе будут принимать только дескрипторы контекста, созданные методом этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="526c5-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 





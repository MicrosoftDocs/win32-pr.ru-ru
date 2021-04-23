---
title: R (RPC)
description: Слова, начинающиеся с R в глоссарии удаленного вызова процедур (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7c1eadf9-367f-45c7-82a0-e410e7f58868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1274d180faefda3f0fe1d8441b69c815361e305a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414477"
---
# <a name="r-rpc"></a><span data-ttu-id="60dbd-103">R (RPC)</span><span class="sxs-lookup"><span data-stu-id="60dbd-103">R (RPC)</span></span>

<span data-ttu-id="60dbd-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G р [. J](i-glos.md) K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) R [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="60dbd-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) R [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="60dbd-105"><span id="_rpc_rpc_object_glos"></span><span id="_RPC_RPC_OBJECT_GLOS"></span>**Объект RPC**</span><span class="sxs-lookup"><span data-stu-id="60dbd-105"><span id="_rpc_rpc_object_glos"></span><span id="_RPC_RPC_OBJECT_GLOS"></span>**RPC object**</span></span>
</dt> <dd>

<span data-ttu-id="60dbd-106">Экземпляры сервера или другие ресурсы, такие как устройства, базы данных и очереди, которые работают и управляются приложениями RPC-Server.</span><span class="sxs-lookup"><span data-stu-id="60dbd-106">Server instances or other resources, such as devices, databases, and queues, that are operated on and managed by RPC-server applications.</span></span> <span data-ttu-id="60dbd-107">Каждый объект однозначно идентифицируется одним или несколькими идентификаторами UUID объекта.</span><span class="sxs-lookup"><span data-stu-id="60dbd-107">Each object is uniquely identified by one or more object UUIDs.</span></span>

</dd> <dt>

<span data-ttu-id="60dbd-108"><span id="_rpc_rpcss_glos"></span><span id="_RPC_RPCSS_GLOS"></span>**Подсистема RPC (RPCSS)**</span><span class="sxs-lookup"><span data-stu-id="60dbd-108"><span id="_rpc_rpcss_glos"></span><span id="_RPC_RPCSS_GLOS"></span>**RPC Subsystem (RPCSS)**</span></span>
</dt> <dd>

<span data-ttu-id="60dbd-109">Подсистема Windows, которая включает в себя различные службы RPC и OLE, включая сопоставитель конечных точек, диспетчер управления OLE-служб (SCM) и сопоставитель объектов COM.</span><span class="sxs-lookup"><span data-stu-id="60dbd-109">Windows subsystem that includes a variety of RPC and OLE services, including the endpoint mapper, OLE Service Control Manager (SCM), and the COM Object Resolver.</span></span> <span data-ttu-id="60dbd-110">Не путайте это с пакетом выделения памяти, характерным для RPC, и RPCSS.</span><span class="sxs-lookup"><span data-stu-id="60dbd-110">Do not confuse this with the RPC-specific memory allocator package, RpcSs.</span></span>

</dd> <dt>

<span data-ttu-id="60dbd-111"><span id="_rpc_reference_pointer_glos"></span><span id="_RPC_REFERENCE_POINTER_GLOS"></span>**указатель ссылки**</span><span class="sxs-lookup"><span data-stu-id="60dbd-111"><span id="_rpc_reference_pointer_glos"></span><span id="_RPC_REFERENCE_POINTER_GLOS"></span>**reference pointer**</span></span>
</dt> <dd>

<span data-ttu-id="60dbd-112">Простейший тип указателя.</span><span class="sxs-lookup"><span data-stu-id="60dbd-112">Simplest pointer type.</span></span> <span data-ttu-id="60dbd-113">Указатель ссылки всегда указывает на допустимое хранилище, и это хранилище не изменяется (хотя содержимое может измениться).</span><span class="sxs-lookup"><span data-stu-id="60dbd-113">A reference pointer always points to valid storage and that storage does not change (although the contents may change).</span></span> <span data-ttu-id="60dbd-114">Указатель ссылки не может быть псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="60dbd-114">A reference pointer cannot be aliased.</span></span> <span data-ttu-id="60dbd-115">Атрибут \[ [ref](/windows/desktop/Midl/ref) \] обозначает указатель ссылки.</span><span class="sxs-lookup"><span data-stu-id="60dbd-115">The \[ [ref](/windows/desktop/Midl/ref)\] attribute designates a reference pointer.</span></span> <span data-ttu-id="60dbd-116">См. также [*уникальный указатель*](u-glos.md) и [*полный указатель*](f-glos.md).</span><span class="sxs-lookup"><span data-stu-id="60dbd-116">See also [*unique pointer*](u-glos.md) and [*full pointer*](f-glos.md).</span></span>

</dd> </dl>

 

 

---
description: Сочетание одного или нескольких параметров блокировки, описывающих тип выполняемой блокировки.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999431"
---
# <a name="d3dlock"></a><span data-ttu-id="66ce0-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="66ce0-103">D3DLOCK</span></span>

<span data-ttu-id="66ce0-104">Сочетание одного или нескольких параметров блокировки, описывающих тип выполняемой блокировки.</span><span class="sxs-lookup"><span data-stu-id="66ce0-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="66ce0-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="66ce0-105">\#define</span></span>                   | <span data-ttu-id="66ce0-106">Описание</span><span class="sxs-lookup"><span data-stu-id="66ce0-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ce0-107">D3DLOCK \_ отбросить</span><span class="sxs-lookup"><span data-stu-id="66ce0-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="66ce0-108">Приложение отклоняет всю память в заблокированном регионе.</span><span class="sxs-lookup"><span data-stu-id="66ce0-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="66ce0-109">Для буферов вершин и индексов весь буфер будет удален.</span><span class="sxs-lookup"><span data-stu-id="66ce0-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="66ce0-110">Этот параметр допустим только при создании ресурса с динамическим использованием (см. [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="66ce0-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="66ce0-111">D3DLOCK \_ донотваит</span><span class="sxs-lookup"><span data-stu-id="66ce0-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="66ce0-112">Позволяет приложению получать циклы ЦП, если драйвер не может немедленно заблокировать рабочую область.</span><span class="sxs-lookup"><span data-stu-id="66ce0-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="66ce0-113">Если этот флаг установлен и драйвер не может немедленно заблокировать поверхность, вызов блокировки возвратит D3DERR \_ васстиллдравинг.</span><span class="sxs-lookup"><span data-stu-id="66ce0-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="66ce0-114">Этот флаг можно использовать только при блокировке поверхности, созданной с помощью [**креатеоффскринплаинсурфаце**](/windows/desktop/api), [**креатерендертаржет**](/windows/desktop/api)или [**креатедепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="66ce0-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="66ce0-115">Этот флаг также можно использовать с задним буфером.</span><span class="sxs-lookup"><span data-stu-id="66ce0-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="66ce0-116">D3DLOCK \_ без \_ "грязного" \_ обновления</span><span class="sxs-lookup"><span data-stu-id="66ce0-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="66ce0-117">По умолчанию блокировка ресурса добавляет к этому ресурсу «грязную» область.</span><span class="sxs-lookup"><span data-stu-id="66ce0-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="66ce0-118">Этот параметр предотвращает любые изменения в «грязном» состоянии ресурса.</span><span class="sxs-lookup"><span data-stu-id="66ce0-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="66ce0-119">Приложения должны использовать этот параметр, если у них есть дополнительные сведения о наборе регионов, измененных во время операции блокировки.</span><span class="sxs-lookup"><span data-stu-id="66ce0-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="66ce0-120">D3DLOCK \_ нуверврите</span><span class="sxs-lookup"><span data-stu-id="66ce0-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="66ce0-121">Указывает, что память, на которую ссылается вызов рисования с момента последней блокировки без этого флага, не будет изменена во время блокировки.</span><span class="sxs-lookup"><span data-stu-id="66ce0-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="66ce0-122">Это может включить оптимизацию, когда приложение добавляет данные к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="66ce0-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="66ce0-123">Если указать этот флаг, драйвер будет немедленно возвращаться, если ресурс используется. в противном случае драйвер должен завершить использовать ресурс перед возвратом из блокировки.</span><span class="sxs-lookup"><span data-stu-id="66ce0-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="66ce0-124">D3DLOCK \_ носислокк</span><span class="sxs-lookup"><span data-stu-id="66ce0-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="66ce0-125">Поведением по умолчанию блокировки видеопамяти является резервирование критической секции на уровне системы, гарантирующая, что в течение блокировки не произойдет никаких изменений режима просмотра.</span><span class="sxs-lookup"><span data-stu-id="66ce0-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="66ce0-126">Этот параметр приводит к тому, что критически важный для всей системы раздел не будет удерживаться на время блокировки.</span><span class="sxs-lookup"><span data-stu-id="66ce0-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="66ce0-127">Операция блокировки занимает много времени, но может позволить системе выполнять другие обязанности, например перемещать курсор мыши.</span><span class="sxs-lookup"><span data-stu-id="66ce0-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="66ce0-128">Этот параметр полезен для долгосрочных блокировок, таких как блокировка заднего буфера для отрисовки программного обеспечения, которая в противном случае негативно повлияет на скорость реагирования системы.</span><span class="sxs-lookup"><span data-stu-id="66ce0-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="66ce0-129">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="66ce0-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="66ce0-130">Приложение не будет записывать в буфер.</span><span class="sxs-lookup"><span data-stu-id="66ce0-130">The application will not write to the buffer.</span></span> <span data-ttu-id="66ce0-131">Это позволяет ресурсам, хранящимся в несобственных форматах, сохранять шаг повторного сжатия при разблокировании.</span><span class="sxs-lookup"><span data-stu-id="66ce0-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="66ce0-132">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="66ce0-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="66ce0-133">Header</span><span class="sxs-lookup"><span data-stu-id="66ce0-133">Header</span></span>                   | <span data-ttu-id="66ce0-134">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="66ce0-134">d3d9types.h</span></span> |
| <span data-ttu-id="66ce0-135">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="66ce0-135">Minimum operating system</span></span> | <span data-ttu-id="66ce0-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="66ce0-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="66ce0-137">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="66ce0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66ce0-138">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="66ce0-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="66ce0-139">**локкрект**</span><span class="sxs-lookup"><span data-stu-id="66ce0-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="66ce0-140">**Блокировка**</span><span class="sxs-lookup"><span data-stu-id="66ce0-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="66ce0-141">**локкрект**</span><span class="sxs-lookup"><span data-stu-id="66ce0-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="66ce0-142">**локкрект**</span><span class="sxs-lookup"><span data-stu-id="66ce0-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="66ce0-143">**Блокировка**</span><span class="sxs-lookup"><span data-stu-id="66ce0-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="66ce0-144">**Хранилища**</span><span class="sxs-lookup"><span data-stu-id="66ce0-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="66ce0-145">**Хранилища**</span><span class="sxs-lookup"><span data-stu-id="66ce0-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="66ce0-146">**локкиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="66ce0-147">**локквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="66ce0-148">**локквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="66ce0-149">**локкаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="66ce0-150">**локкаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="66ce0-151">**локкиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="66ce0-152">**локквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="66ce0-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 

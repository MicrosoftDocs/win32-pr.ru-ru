---
description: С помощью поверхности можно хранить данные любого типа для конкретного приложения. Например, поверхность, представляющая карту в игре, может содержать сведения о ландшафта.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Частные данные поверхности (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710685"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="011e0-104">Частные данные поверхности (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="011e0-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="011e0-105">С помощью поверхности можно хранить данные любого типа для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="011e0-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="011e0-106">Например, поверхность, представляющая карту в игре, может содержать сведения о ландшафта.</span><span class="sxs-lookup"><span data-stu-id="011e0-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="011e0-107">Поверхность может иметь более одного закрытого буфера данных.</span><span class="sxs-lookup"><span data-stu-id="011e0-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="011e0-108">Каждый буфер идентифицируется по идентификатору GUID, указанному при присоединении данных к поверхности.</span><span class="sxs-lookup"><span data-stu-id="011e0-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="011e0-109">Чтобы сохранить данные частной поверхности, используйте Сетприватедата, передав указатель на исходный буфер, размер данных и определяемый приложением идентификатор GUID для данных.</span><span class="sxs-lookup"><span data-stu-id="011e0-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="011e0-110">При необходимости исходные данные могут существовать в виде COM-объекта. в этом случае вы передаете указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) объекта и устанавливаете \_ флаг D3DSPD иункновнпоинтер.</span><span class="sxs-lookup"><span data-stu-id="011e0-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="011e0-111">Сетприватедата выделяет внутренний буфер для данных и копирует его.</span><span class="sxs-lookup"><span data-stu-id="011e0-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="011e0-112">Затем можно безопасно освободить исходный буфер или объект.</span><span class="sxs-lookup"><span data-stu-id="011e0-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="011e0-113">Ссылка на внутренний буфер или интерфейс освобождается при вызове Фриприватедата.</span><span class="sxs-lookup"><span data-stu-id="011e0-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="011e0-114">Это происходит автоматически при освобождении поверхности.</span><span class="sxs-lookup"><span data-stu-id="011e0-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="011e0-115">Чтобы получить закрытые данные для поверхности, необходимо выделить буфер правильного размера, а затем вызвать метод Жетприватедата, передав ему идентификатор GUID, который был назначен данным.</span><span class="sxs-lookup"><span data-stu-id="011e0-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="011e0-116">Вы несете ответственность за освобождение любой динамической памяти, используемой для этого буфера.</span><span class="sxs-lookup"><span data-stu-id="011e0-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="011e0-117">Если данные являются COM-объектом, этот метод извлекает указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="011e0-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="011e0-118">Если неизвестно, насколько велик буфер для выделения, сначала вызовите Жетприватедата с нулевым значением в Псизеофдата.</span><span class="sxs-lookup"><span data-stu-id="011e0-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="011e0-119">Если метод завершается с ошибкой D3DERR \_ MOREDATA, он возвращает необходимое число байтов для буфера.</span><span class="sxs-lookup"><span data-stu-id="011e0-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="011e0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="011e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="011e0-121">Поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="011e0-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 

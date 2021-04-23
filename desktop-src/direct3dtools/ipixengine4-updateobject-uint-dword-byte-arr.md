---
description: Обновляет начальное состояние объекта; Например, текстура или шейдер.
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine4:: UpdateObject'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f21bac93bea44cb7226897a89460788c3900b8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494691"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span data-ttu-id="86028-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>Метод IPixEngine4:: UpdateObject</span><span class="sxs-lookup"><span data-stu-id="86028-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4::UpdateObject method</span></span>

<span data-ttu-id="86028-104">Обновляет начальное состояние объекта; Например, текстура или шейдер.</span><span class="sxs-lookup"><span data-stu-id="86028-104">Updates the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="86028-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86028-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="86028-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86028-106">Parameters</span></span>

<span data-ttu-id="86028-107">*обжектаддресс* </span><span class="sxs-lookup"><span data-stu-id="86028-107">*objectAddress* </span></span>  
<span data-ttu-id="86028-108">Идентификатор обновляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="86028-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="86028-109">*изменять* </span><span class="sxs-lookup"><span data-stu-id="86028-109">*size* </span></span>  
<span data-ttu-id="86028-110">Размер полезных данных обновления в байтах.</span><span class="sxs-lookup"><span data-stu-id="86028-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="86028-111">*\_буфер count1* </span><span class="sxs-lookup"><span data-stu-id="86028-111">*count1\_buffer* </span></span>  
<span data-ttu-id="86028-112">Полезные данные обновления.</span><span class="sxs-lookup"><span data-stu-id="86028-112">The update payload.</span></span>

## <a name="return-value"></a><span data-ttu-id="86028-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86028-113">Return value</span></span>

<span data-ttu-id="86028-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="86028-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86028-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86028-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86028-116">Требования</span><span class="sxs-lookup"><span data-stu-id="86028-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="86028-117">Header</span><span class="sxs-lookup"><span data-stu-id="86028-117">Header</span></span></p></td><td><span data-ttu-id="86028-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="86028-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="86028-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="86028-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="86028-120">**IPixEngine4**</span><span class="sxs-lookup"><span data-stu-id="86028-120">**IPixEngine4**</span></span>](/windows/desktop/direct3dtools/ipixengine4)

 

 

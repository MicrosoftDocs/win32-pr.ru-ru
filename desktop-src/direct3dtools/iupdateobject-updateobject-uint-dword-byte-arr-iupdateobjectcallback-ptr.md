---
description: Запрос на обновление первоначального состояния объекта; Например, текстура или шейдер.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иупдатеобжект:: UpdateObject'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495252"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="d304a-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>Метод Иупдатеобжект:: UpdateObject</span><span class="sxs-lookup"><span data-stu-id="d304a-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="d304a-104">Запрос на обновление первоначального состояния объекта; Например, текстура или шейдер.</span><span class="sxs-lookup"><span data-stu-id="d304a-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d304a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d304a-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="d304a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d304a-106">Parameters</span></span>

<span data-ttu-id="d304a-107">*обжектаддресс* </span><span class="sxs-lookup"><span data-stu-id="d304a-107">*objectAddress* </span></span>  
<span data-ttu-id="d304a-108">Идентификатор обновляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="d304a-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="d304a-109">*изменять* </span><span class="sxs-lookup"><span data-stu-id="d304a-109">*size* </span></span>  
<span data-ttu-id="d304a-110">Размер полезных данных обновления в байтах.</span><span class="sxs-lookup"><span data-stu-id="d304a-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="d304a-111">*\_буфер count1* </span><span class="sxs-lookup"><span data-stu-id="d304a-111">*count1\_buffer* </span></span>  
<span data-ttu-id="d304a-112">Полезные данные обновления.</span><span class="sxs-lookup"><span data-stu-id="d304a-112">The update payload.</span></span>

<span data-ttu-id="d304a-113">*пкаллбакк* </span><span class="sxs-lookup"><span data-stu-id="d304a-113">*pCallback* </span></span>  
<span data-ttu-id="d304a-114">Адрес функции, используемой для уведомления узла о том, что объект был обновлен.</span><span class="sxs-lookup"><span data-stu-id="d304a-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="d304a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d304a-115">Return value</span></span>

<span data-ttu-id="d304a-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d304a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d304a-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d304a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d304a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d304a-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d304a-119">Header</span><span class="sxs-lookup"><span data-stu-id="d304a-119">Header</span></span></p></td><td><span data-ttu-id="d304a-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="d304a-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d304a-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="d304a-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d304a-122">**иупдатеобжект**</span><span class="sxs-lookup"><span data-stu-id="d304a-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 

---
description: Освобождает текстуру и уведомляет узел асинхронно.
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Фритекстуреасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aed7d29653b9da6f39b1ef6ec4e600c1857744f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495684"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span data-ttu-id="5f26e-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Фритекстуреасинк</span><span class="sxs-lookup"><span data-stu-id="5f26e-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::FreeTextureAsync method</span></span>

<span data-ttu-id="5f26e-104">Освобождает текстуру и уведомляет узел асинхронно.</span><span class="sxs-lookup"><span data-stu-id="5f26e-104">Frees a texture and notifies the host asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f26e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f26e-105">Syntax</span></span>


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5f26e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f26e-106">Parameters</span></span>

<span data-ttu-id="5f26e-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="5f26e-107">*textureId* </span></span>  
<span data-ttu-id="5f26e-108">Идентификатор свободной текстуры.</span><span class="sxs-lookup"><span data-stu-id="5f26e-108">The ID of the texture to free..</span></span>

<span data-ttu-id="5f26e-109">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="5f26e-109">*callbacks* </span></span>  
<span data-ttu-id="5f26e-110">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="5f26e-110">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="5f26e-111">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="5f26e-111">*requestCookie* </span></span>  
<span data-ttu-id="5f26e-112">Файл cookie, который уникально иденфиес запрос, и может использоваться для оповещения об отмене.</span><span class="sxs-lookup"><span data-stu-id="5f26e-112">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="5f26e-113">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="5f26e-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5f26e-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5f26e-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f26e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f26e-115">Return value</span></span>

<span data-ttu-id="5f26e-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f26e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f26e-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f26e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f26e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5f26e-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5f26e-119">Header</span><span class="sxs-lookup"><span data-stu-id="5f26e-119">Header</span></span></p></td><td><span data-ttu-id="5f26e-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5f26e-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5f26e-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5f26e-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5f26e-122">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="5f26e-122">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

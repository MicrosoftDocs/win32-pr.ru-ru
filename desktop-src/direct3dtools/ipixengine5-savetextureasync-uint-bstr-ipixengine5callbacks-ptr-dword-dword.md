---
description: Сохраняет текстуру.
MS-HAID: vspixengine.IPixEngine5\_SaveTextureAsync\_UINT\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Саветекстуреасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6F08F49E-6FFD-4A9B-86F5-8CB499947F57
api_name:
- IPixEngine5.SaveTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2590f793d0ba05af1ccf9e10ba04fa8b6aa2421b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495729"
---
# <a name="span-idvspixengineipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5savetextureasync-method"></a><span data-ttu-id="dde6d-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Саветекстуреасинк</span><span class="sxs-lookup"><span data-stu-id="dde6d-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::SaveTextureAsync method</span></span>

<span data-ttu-id="dde6d-104">Сохраняет текстуру.</span><span class="sxs-lookup"><span data-stu-id="dde6d-104">Saves a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dde6d-105">Syntax</span></span>


```C++
HRESULT SaveTextureAsync(
   UINT                  textureId,
   BSTR                  fileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="dde6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dde6d-106">Parameters</span></span>

<span data-ttu-id="dde6d-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="dde6d-107">*textureId* </span></span>  
<span data-ttu-id="dde6d-108">Идентификатор текстуры для сохранения.</span><span class="sxs-lookup"><span data-stu-id="dde6d-108">The ID of the texture to save.</span></span>

<span data-ttu-id="dde6d-109">*Файлов* </span><span class="sxs-lookup"><span data-stu-id="dde6d-109">*fileName* </span></span>  
<span data-ttu-id="dde6d-110">Строка COM, содержащая путь к сохраненной текстуре.</span><span class="sxs-lookup"><span data-stu-id="dde6d-110">A COM string containing the pathname of the saved texture.</span></span>

<span data-ttu-id="dde6d-111">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="dde6d-111">*callbacks* </span></span>  
<span data-ttu-id="dde6d-112">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="dde6d-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="dde6d-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="dde6d-113">*requestCookie* </span></span>  
<span data-ttu-id="dde6d-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="dde6d-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="dde6d-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="dde6d-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="dde6d-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="dde6d-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="dde6d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dde6d-117">Return value</span></span>

<span data-ttu-id="dde6d-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dde6d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dde6d-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dde6d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde6d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dde6d-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dde6d-121">Header</span><span class="sxs-lookup"><span data-stu-id="dde6d-121">Header</span></span></p></td><td><span data-ttu-id="dde6d-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="dde6d-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dde6d-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="dde6d-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dde6d-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="dde6d-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

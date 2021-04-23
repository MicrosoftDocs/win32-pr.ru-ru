---
description: Завершает обработку для создания декодированного изображения.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'Метод IDirect3DDXVADevice9:: Ендфраме (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155190"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="c0053-103">Метод IDirect3DDXVADevice9:: Ендфраме</span><span class="sxs-lookup"><span data-stu-id="c0053-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="c0053-104">Завершает обработку для создания декодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="c0053-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0053-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0053-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="c0053-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0053-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0053-107">*сиземискдата*</span><span class="sxs-lookup"><span data-stu-id="c0053-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="c0053-108">Размер буфера, заданного параметром *пмискдата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="c0053-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="c0053-109">Значение должно быть равно 2.</span><span class="sxs-lookup"><span data-stu-id="c0053-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="c0053-110">*пмискдата*</span><span class="sxs-lookup"><span data-stu-id="c0053-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="c0053-111">Указатель на буфер, содержащий данные для ускорителя видео.</span><span class="sxs-lookup"><span data-stu-id="c0053-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="c0053-112">Этот буфер должен содержать тот же индекс кадра, который был передан методу [**IDirect3DDXVADevice9:: бегинфраме**](idirect3ddxvadevice9-beginframe.md) в параметре *пинпутдата* .</span><span class="sxs-lookup"><span data-stu-id="c0053-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0053-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0053-113">Return value</span></span>

<span data-ttu-id="c0053-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c0053-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0053-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0053-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0053-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c0053-116">Requirements</span></span>



| <span data-ttu-id="c0053-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c0053-117">Requirement</span></span> | <span data-ttu-id="c0053-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c0053-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c0053-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0053-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0053-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0053-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0053-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0053-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0053-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0053-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0053-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0053-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0053-124"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0053-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0053-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0053-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0053-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="c0053-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 





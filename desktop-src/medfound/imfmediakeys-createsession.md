---
description: Создает объект сеанса ключа мультимедиа, используя указанные данные инициализации и пользовательские данные. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'Метод Имфмедиакэйс:: CreateSession'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693873"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="fb699-104">Метод Имфмедиакэйс:: CreateSession</span><span class="sxs-lookup"><span data-stu-id="fb699-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="fb699-105">Создает объект сеанса ключа мультимедиа, используя указанные данные инициализации и пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="fb699-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="fb699-106">.</span><span class="sxs-lookup"><span data-stu-id="fb699-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb699-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb699-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="fb699-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb699-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb699-109">*Успешности*</span><span class="sxs-lookup"><span data-stu-id="fb699-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-110">Тип MIME контейнера мультимедиа, используемого для содержимого.</span><span class="sxs-lookup"><span data-stu-id="fb699-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="fb699-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="fb699-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-112">Данные инициализации для системы ключей.</span><span class="sxs-lookup"><span data-stu-id="fb699-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="fb699-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="fb699-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-114">Число в байтах *initdata*.</span><span class="sxs-lookup"><span data-stu-id="fb699-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="fb699-115">*Пользовательские*</span><span class="sxs-lookup"><span data-stu-id="fb699-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-116">Пользовательские данные, отправляемые в систему ключей.</span><span class="sxs-lookup"><span data-stu-id="fb699-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="fb699-117">*кбкустомдата*</span><span class="sxs-lookup"><span data-stu-id="fb699-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-118">Число в байтах *кбкустомдата*.</span><span class="sxs-lookup"><span data-stu-id="fb699-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="fb699-119">*явлении*</span><span class="sxs-lookup"><span data-stu-id="fb699-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-120">явлении</span><span class="sxs-lookup"><span data-stu-id="fb699-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="fb699-121">*ппсессион*</span><span class="sxs-lookup"><span data-stu-id="fb699-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="fb699-122">Сеанс ключа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fb699-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb699-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb699-123">Return value</span></span>

<span data-ttu-id="fb699-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fb699-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb699-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb699-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb699-126">Требования</span><span class="sxs-lookup"><span data-stu-id="fb699-126">Requirements</span></span>



| <span data-ttu-id="fb699-127">Требование</span><span class="sxs-lookup"><span data-stu-id="fb699-127">Requirement</span></span> | <span data-ttu-id="fb699-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fb699-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb699-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb699-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb699-130">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb699-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb699-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb699-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb699-132">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb699-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fb699-133">IDL</span><span class="sxs-lookup"><span data-stu-id="fb699-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb699-134"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb699-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb699-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb699-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb699-136">**имфмедиакэйс**</span><span class="sxs-lookup"><span data-stu-id="fb699-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 





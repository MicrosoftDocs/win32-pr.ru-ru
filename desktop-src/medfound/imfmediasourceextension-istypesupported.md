---
description: Возвращает значение, указывающее, поддерживается ли указанный тип MIME источником мультимедиа.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Метод Имфмедиасаурцеекстенсион:: Истипесуппортед'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693864"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="bd43b-103">Метод Имфмедиасаурцеекстенсион:: Истипесуппортед</span><span class="sxs-lookup"><span data-stu-id="bd43b-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="bd43b-104">Возвращает значение, указывающее, поддерживается ли указанный тип MIME источником мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bd43b-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd43b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd43b-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="bd43b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd43b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd43b-107">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bd43b-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd43b-108">Тип носителя для проверки поддержки.</span><span class="sxs-lookup"><span data-stu-id="bd43b-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd43b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd43b-109">Return value</span></span>

<span data-ttu-id="bd43b-110">**значение true** , если тип мультимедиа поддерживается; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="bd43b-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd43b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bd43b-111">Requirements</span></span>



| <span data-ttu-id="bd43b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="bd43b-112">Requirement</span></span> | <span data-ttu-id="bd43b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bd43b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd43b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd43b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bd43b-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd43b-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd43b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd43b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bd43b-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd43b-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bd43b-118">IDL</span><span class="sxs-lookup"><span data-stu-id="bd43b-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd43b-119"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd43b-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd43b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd43b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd43b-121">**имфмедиасаурцеекстенсион**</span><span class="sxs-lookup"><span data-stu-id="bd43b-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




